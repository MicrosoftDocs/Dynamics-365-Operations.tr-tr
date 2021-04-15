---
title: ER kullanarak elektronik belgeler oluşturma ve uygulama verilerini güncelleştirme
description: Giden elektronik belgeler oluşturmak için uygulamada kullanılabilen Elektronik raporlama (ER) biçimlerini tasarlayabilirsiniz.
author: NickSelin
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 863c69446e9a7d447847483ec129788e85a8fd58
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750046"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="7abba-103">ER kullanarak elektronik belgeler oluşturma ve uygulama verilerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7abba-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7abba-104">Giden elektronik belgeler oluşturmak için uygulamada kullanılabilen Elektronik raporlama (ER) biçimlerini tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7abba-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="7abba-105">Ayrıca gelen elektronik belgeleri ayrıştıran ER biçimleri tasarlayabilir ve bu belgelerdeki içerikleri uygulama verisini güncelleştirmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7abba-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="7abba-106">Bu işlev ile tek bir ER biçimi giden elektronik belgeleri oluşturmak ve daha sonra uygulama verisini güncelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7abba-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="7abba-107">Bu özellik aşağıdaki senaryolarda kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="7abba-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="7abba-108">Uygulama verisinin yinelenen işlemlerde kullanılmasını engellemek için bir uygulamanın verisini elektronik belgeler oluşturmak için kullanıldıktan hemen sonra işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7abba-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="7abba-109">Örneğin, ödeme hareketlerini, bir oluşturulan ödeme iletisine dahil edilmelerinden sonra derhal zaten işlendi olarak işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7abba-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="7abba-110">ER mantığı kullanılarak oluşturulmuş elektronik belgelerin ayrıntılarını depolamak için.</span><span class="sxs-lookup"><span data-stu-id="7abba-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="7abba-111">Örneğin, ER ifadesi kullanılarak oluşturuluş bir benzersiz ödeme ileti kimlik saptaması.</span><span class="sxs-lookup"><span data-stu-id="7abba-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="7abba-112">İfade, ER biçimi belgeleri oluşturmak için çalıştırıldığında, ER iletişim kutusunda girilen bilgiye dayanır.</span><span class="sxs-lookup"><span data-stu-id="7abba-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="7abba-113">Bu özellik hakkında daha fazla bilgi için Intrastat raporlama ve arşivleme ayrıntıları hakkında sizi bilgilendirecek ER Uygulama veri güncelleştirmesi ile belgeler oluşturma Görev kılavuzlarını (7.5.4.3 Al/Geliş BT hizmeti/çözüm bileşenleri (10677) iş işleminin parçası olarak) oynatın.</span><span class="sxs-lookup"><span data-stu-id="7abba-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="7abba-114">Aşağıdaki dosyalar, bu Görev kılavuzlarındaki çeşitli adımları tamamlamak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7abba-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="7abba-115">Bu dosyaları yerel makinenize indirin ve kaydedin.</span><span class="sxs-lookup"><span data-stu-id="7abba-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="7abba-116">ER veri modeli konfigürasyonu: Intrastat (model)</span><span class="sxs-lookup"><span data-stu-id="7abba-116">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="7abba-117">ER model eşleme yapılandırması: Intrastat (eşleme)</span><span class="sxs-lookup"><span data-stu-id="7abba-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="7abba-118">ER biçim yapılandırma: Intrastat (biçim)</span><span class="sxs-lookup"><span data-stu-id="7abba-118">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]