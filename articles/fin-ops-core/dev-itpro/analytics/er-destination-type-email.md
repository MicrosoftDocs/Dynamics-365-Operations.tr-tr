---
title: E-posta ER hedef türü
description: Bu konu, giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için bir e-posta hedefinin nasıl yapılandırılacağı hakkında bilgi sağlamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72f67ad915ba2acc90ecb52bdb97e42504450a03
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745573"
---
# <a name="email-destination"></a><span data-ttu-id="cb467-103">E-posta hedefi</span><span class="sxs-lookup"><span data-stu-id="cb467-103">Email destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb467-104">Giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için bir e-posta hedefi yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb467-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="cb467-105">Hedef ayarına bağlı olarak, oluşturulan bir belge elektronik posta eki olarak teslim edilir.</span><span class="sxs-lookup"><span data-stu-id="cb467-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="cb467-106">E-posta ile bir çıkış dosyası göndermek için **Etkin** değerini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cb467-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="cb467-107">Bu seçenek etkinleştirildikten sonra e-posta konusunu ve metnini düzenleyebilir ve e-posta alıcılarını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb467-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="cb467-108">E-posta metni ve konusu için sabit metinler ayarlayabilir veya ER [formüllerini](er-formula-language.md) kullanarak dinamik e-posta metinleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb467-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="cb467-109">E-posta adreslerini ER içerisinde iki şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb467-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="cb467-110">Yapılandırma, aynen Yazdırma yönetimi özelliğinin tamamladığı şekilde tamamlanabilir veya bir formülle bir e-posta yapılandırmasına doğrudan başvuru kullanarak bir e-posta adresini çözümleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb467-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="cb467-111">[![E-posta hedefini etkinleştirme](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="cb467-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="cb467-112">E-posta adresi türleri</span><span class="sxs-lookup"><span data-stu-id="cb467-112">Email address types</span></span>

<span data-ttu-id="cb467-113">**Giden** veya **Bilgi** alanlarında **Düzenle**'yi seçtiğiniz zaman **E-posta at** iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="cb467-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="cb467-114">Daha sonra kullanılacak e-posta adresi türünü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb467-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="cb467-115">Şu anda **Yapılandırma e-postası** ve **Yazdırma Yönetimi** e-posta türleri destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="cb467-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="cb467-116">[![E-posta türü seçme](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="cb467-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="cb467-117">Yazdırma yönetimi</span><span class="sxs-lookup"><span data-stu-id="cb467-117">Print management</span></span>

<span data-ttu-id="cb467-118">**Yazdırma Yönetimi** e-posta türünü seçerseniz, **Giden** alanına sabit bir e-posta adresi girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb467-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="cb467-119">[![Sabit e-posta adreslerini yapılandırma](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="cb467-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="cb467-120">Sabit olmayan e-posta adreslerini kullanmak amacıyla bir dosya hedefi için e-posta kaynak türünü seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="cb467-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="cb467-121">Aşağıdaki değerler desteklenir: **Müşteri**, **Satıcı**, **Müşteri Adayı**, **İlgili kişi**, **Rakip**, **Çalışan**, **Başvuran**, **Satıcı adayı** ve **Onaylanmamış satıcı**.</span><span class="sxs-lookup"><span data-stu-id="cb467-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="cb467-122">Bir e-posta kaynak türü seçtikten sonra **Formül tasarımcısı** formunu açmak için **E-posta kaynak hesabı** alanının yanındaki düğmeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb467-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="cb467-123">Bu formu çalışma zamanında dönen bir formülü, seçilen kaynak türünün **taraf hesabını** işlenmiş belgeden e-posta hedefine iliştirmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb467-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="cb467-124">[![E-posta kaynağı hesabını yapılandırma](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="cb467-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="cb467-125">Formüller ER yapılandırmasına özgüdür.</span><span class="sxs-lookup"><span data-stu-id="cb467-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="cb467-126">**Formül** alanında bir müşteri veya satıcı tarafı türü için belgeye özgü bir referans girin.</span><span class="sxs-lookup"><span data-stu-id="cb467-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="cb467-127">Yazmak yerine, müşteri veya satıcı hesabını temsil eden bir veri kaynağı düğümünü bulabilir ve sonra formülü güncelleştirmek için **Veri kaynağı ekle**'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb467-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="cb467-128">Örneğin, **ISO 20022 Borç Transferi** yapılandırmasını kullanıyorsanız bir satıcı hesabını temsil eden düğüm `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID` olur.</span><span class="sxs-lookup"><span data-stu-id="cb467-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="cb467-129">`"DE-001"` gibi bir dize değeri girer ve bir formül kaydederseniz, satıcının ilgili kişisine ( **DE-001**) bir e-posta gönderilir.</span><span class="sxs-lookup"><span data-stu-id="cb467-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="cb467-130">[![ER formül tasarımcısı sayfası](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="cb467-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="cb467-131">[![E-posta kaynağı öznitelik hesabını yapılandırma](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="cb467-131">[![Configure email source attributes account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="cb467-132">Konfigürasyon e-postası</span><span class="sxs-lookup"><span data-stu-id="cb467-132">Configuration email</span></span>

<span data-ttu-id="cb467-133">Kullandığınız yapılandırma, veri kaynaklarında bir **e-posta adresini** döndüren bir düğüme sahipse bu e-posta türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb467-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="cb467-134">Formül tasarımcısında veri kaynaklarını ve fonksiyonları, doğru şekilde biçimlendirilmiş bir e-posta adresi elde etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb467-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="cb467-135">Örneğin, **ISO 20022 Borç Transferi** yapılandırmasını kullanıyorsanız bir satıcının ilgili kişi e-posta adresini temsil eden düğüm `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email` olur.</span><span class="sxs-lookup"><span data-stu-id="cb467-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="cb467-136">[![E-posta adresi kaynağını yapılandırma](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="cb467-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb467-137">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cb467-137">Additional resources</span></span>

- [<span data-ttu-id="cb467-138">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="cb467-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="cb467-139">Elektronik raporlama (ER) hedefleri</span><span class="sxs-lookup"><span data-stu-id="cb467-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="cb467-140">Elektronik raporlamada (ER) formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="cb467-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
