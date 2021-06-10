---
title: Office'te mali günlük şablonlarını açma
description: Bu konuda, bir Microsoft Excel şablonu kullanarak özel mali günlükler oluşturduğunuzda oluşabilecek sorunlar açıklanmaktadır.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089469"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="b9e15-103">Office'te mali günlük şablonlarını açma</span><span class="sxs-lookup"><span data-stu-id="b9e15-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9e15-104">Bu konuda, bir Microsoft Excel şablonu kullanarak özel mali günlükler oluşturduğunuzda oluşabilecek sorunlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b9e15-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="b9e15-105">Belirti</span><span class="sxs-lookup"><span data-stu-id="b9e15-105">Symptom</span></span>

<span data-ttu-id="b9e15-106">Mali günlükler için özel bir Excel şablonu oluşturdunuz ancak **Satırları Excel'de aç** menüsünde görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="b9e15-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="b9e15-107">Alternatif olarak, menüde görünüyor ama seçtiğinizde farklı bir şablon açılıyor.</span><span class="sxs-lookup"><span data-stu-id="b9e15-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="b9e15-108">Çözüm</span><span class="sxs-lookup"><span data-stu-id="b9e15-108">Resolution</span></span>

<span data-ttu-id="b9e15-109">Varsayılan Excel'de Aç işlevi, **Excel'de Aç** menüsünde hangi Office şablonlarının veya veri varlıklarının seçenek olarak görüneceğini belirlemek için geçerli sayfanın kök veri kaynağını (tablo) kullanır.</span><span class="sxs-lookup"><span data-stu-id="b9e15-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="b9e15-110">Bu davranış, mali günlükler için ideal bir deneyim değildir çünkü mali günlükler, diğer birçok günlük türünün kök veri kaynağı olarak aynı tabloları (LedgerJournalTable ve LedgerJournalTrans) kullanır.</span><span class="sxs-lookup"><span data-stu-id="b9e15-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="b9e15-111">Mali günlükler için Excel'de Satırları Aç işlevi, yevmiye defteri veya ödeme günlüğü gibi şu anda bağlamında çalıştığınız günlük için tasarlanmış şablonları göstermek üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b9e15-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="b9e15-112">Örneğin, satıcı ödeme günlüğüyle kullanılması amaçlanan bir şablon, birincil hesabınızı satıcı hesabı olarak zorlamak için tasarlanacak.</span><span class="sxs-lookup"><span data-stu-id="b9e15-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="b9e15-113">Şablonu **Satırları Excel'de Aç** ve **Excel Aç** menülerinde kullanılabilir olacak şekilde tanıtmak istiyorsanız kolay bir geliştirici deneyimi **LedgerIJournalExcelTemplate** arabirimini uygulamak ve **DocuTemplateRegistrationBase** sınıfını genişletmektir.</span><span class="sxs-lookup"><span data-stu-id="b9e15-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="b9e15-114">Bu yaklaşımın birçok örneği sistemde uygulanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b9e15-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="b9e15-115">Referans için kullanılabilecek bir örnek, yevmiye defteri (veya günlük tutulan günlük) için oluşturulan **LedgerDailyJournalExcelTemplate** arabirimidir.</span><span class="sxs-lookup"><span data-stu-id="b9e15-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="b9e15-116">Şablonunuz için **LedgerIJournalExcelTemplate** arabirimi uygulandığında **Satırları Excel'de aç** menüsü şablonları günlüğünüzün günlük türüne göre filtreler ve yalnızca bu günlük için kullanılabilen şablonları gösterir.</span><span class="sxs-lookup"><span data-stu-id="b9e15-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="b9e15-117">Arabirim ayrıca, hesap türü gereksinimlerini karşılamıyorsa bir şablonun günlük için açılamamasını sağlayan bir doğrulama yöntemi sağlar.</span><span class="sxs-lookup"><span data-stu-id="b9e15-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="b9e15-118">Örneğin, hesap türünün **Satıcı** veya **Kayıt Defter** türünde olması gerektiğini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9e15-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="b9e15-119">Bu işlevsellik hakkında daha fazla bilgi için bkz. [Satırları Excel'de Aç menüsüne şablonlar ekleme](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="b9e15-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
