---
title: "Malzeme özel durumlarının görülebilirliği"
description: "Bu konuda, üretim emirleri ve toplu iş emirleri için ham madde özel durumlarının nasıl daha iyi görülebilir duruma getirilebileceği açıklanmaktadır."
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorWorkspace
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validfrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: eca3141fc48aea24411524e5fc84686d9e4bfaa7
ms.contentlocale: tr-tr
ms.lasthandoff: 03/08/2018

---
# <a name="visibility-into-material-exceptions"></a>Malzeme özel durumlarının görülebilirliği

[!include[banner](../includes/banner.md)]

**Üretim katı yönetimi** çalışma alanında bulunan üç kutucuk üretim emirleri ve toplu iş emirleri için ham madde özel durumlarının daha iyi görüntülenebilmesini sağlamanıza olanak tanır.

- Dikkat gerektiren serbest bırakılmamış malzeme satırları
- Dikkat gerektiren işlem görmemiş dalgalar
- Dikkat gerektiren açık ambar işi

Her üç kutucuk için ürün reçetesi (BOM) satırları ve formül satırlarının ham madde tarihi çalışma alanı tarihiyle ve **Çalışma alanımı yapılandır** menüsünde ayarlanmış olan **Üretim birimi**, **Kaynak grubu** ve **Kaynak** alanları filtreleriyle karşılaştırılır. Varsayılan olarak, çalışma alanı tarihi geçerli tarihe ayarlanır ancak bu tarihi düzeltebilirsiniz.

Yayımlanmamış bir ürün reçetesi satırının veya formül satırının, satır hammadde tarihinin çalışma alanı tarihiyle aynı veya bu tarihten önce olduğu ve çalışma alanındaki filtreler tarafından tanımlanan ölçütü karşılayıp karşılamadığı açısından dikkatli şekilde incelenmesi gerekir.

Aşağıdaki şekilde, mavi çubuk kaynakta planlanmış olan bir üretim işimi temsil eder. İş 1 Mayıs 2017 tarihinde (01/05/2017) başlaması için zamanlanır. Bu tarih ham madde tarihidir. Başka bir deyişle, BOM ve formül satırlarında işe atanan malzemelerin bu tarihte hazır olması gerekir. Şekildeki diğer tarih olan 6 Mayıs 2017 (06/05/2017) çalışma alanı tarihini temsil eder. Bu örnekte, ham madde tarihi çalışma alanı tarihinden öncedir. Bu nedenle, hammadde tüketiminin başlangıcı olduğu düşünülen tarih geçmiştir ve ürün reçetesi ve tarih satırları dikkat gösterilmesi için ölçütü karşılamaktadır.

![Ham madde tarihinin çalışma alanı tarihinden önce olduğu bir üretim işi örneği](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a>Dikkat gerektiren serbest bırakılmamış malzeme satırları

Ürün reçetesi veya formül satırı ambara üç şekilde serbest bırakılabilir:

- Üretim emri veya toplu iş emri serbest bırakmanın bir parçası olarak
- El ile serbest bırakma olarak
- Toplu iş aracılığıyla otomatik olarak

Daha fazla bilgi için bkz. [Ürün reçetesi ve formül satırlarını ambara serbest bırakma](releasing-bom-and-formula-lines-to-warehouse.md). 

Bir ürün reçetesi veya formül satırı serbest bırakılmadıysa veya yalnızca kısmen serbest bırakıldıysa ve çalışma alanı tarihi ve filtre ölçütü karşılanıyorsa, satır **Dikkat edilmesi gereken serbest bırakılmamış malzeme satırları** kutucuğunda görüntülenen sayının hesaplanmasına dahil edilir.

Kutucuğu seçtiğinizde, **Ambara serbest bırak** sayfası açılır. Bu sayfada, kutucuktaki sayıyla belirtilen serbest bırakılmamış ürün reçetesi ve formül satırı sayısı gösterilir. Serbest bırakılmayan satırlar yukarıdaki ızgarada gösterilir. Bu ızgara satır için başlangıçta tahmin edilen miktarı, zaten serbest bırakılmış olan miktarı ve hala serbest bırakılması gereken kalan miktarı gösterir. Üst ızgaradan alt ızgaraya satır ekleyebilirsiniz. Alt ızgaradan, seçilen satırları ambara serbest bırakabilirsiniz. Alt ızgaradan, serbest bırakılacak miktarı da ayarlayabilirsiniz. Böylece yalnızca kısmi bir miktar serbest bırakılır.

## <a name="unprocessed-waves-needing-attention"></a>Dikkat gerektiren işlem görmemiş dalgalar

Bir ürün reçetesi veya formül satırı serbest bırakıldığında, üretim dalga şablonu yapılandırmasına bağlı olarak yeni bir üretim dalgasına veya mevcut açık bir dalgaya eklenir. Dalga şablonu yapılandırmasıyla, bir ürün reçetesi veya formül satırı serbest bırakıldığında otomatik olarak işlenecek bir dalga da ayarlayabilirsiniz. Dalga işlendiğinde, ham madde çekme için bir ambar işi oluşturulur. Dalga şablonu, dalgalar serbest bırakma sırasında işlenmeyecek şekilde yapılandırılırsa, dalga işlenmemiş durumda kalır. **Dikkat gerektiren işlem görmemiş dalgalar** kutucuğu işlenmemiş dalgalarda ambara serbest bırakılan ve çalışma alanı tarihiyle aynı veya daha önceki bir tarihte olan bir ham madde tarihi bulunan ürün reçetesi ve formül satırı sayısını gösterir. Ayrıca satırların, çalışma alanı filtresine uygulanan bir işlem kaynağı tarafından tüketilmesi gerekir.

Kutucuk seçildiğinde, **Tüm üretim dalgaları** sayfası açılır. Sayfa, kutucuk ölçütünü karşılayan serbest bırakılmış ürün reçetesi ve formül satırlarından gelen dalga satırları içeren açık dalgaların sayısına göre filtrelenir. **Tüm üretim dalgaları** sayfasından, dalgayı el ile işleyebilirsiniz.

## <a name="open-warehouse-work-needing-attention"></a>Dikkat gerektiren açık ambar işi

**Dikkat gerektiren açık ambar işi** kutucuğu ambara serbest bırakılan, işlenmemiş işi bulunan ve çalışma alanı tarihiyle aynı veya daha önceki bir tarihte olan bir ham madde tarihi bulunan ürün reçetesi ve formül satırı sayısını gösterir. Ayrıca satırların, çalışma alanı filtresine uygulanan bir işlem kaynağı tarafından tüketilmesi gerekir.

Kutucuk seçildiğinde, **Tüm işler** sayfası açılır. Sayfa, kutucuk ölçütünü karşılayan serbest bırakılmış ürün reçetesi ve formül satırlarından gelen iş satırları içeren açık iş başlıklarının sayısına göre filtrelenir. **Tüm işler** sayfasından, işi el ile işleyebilirsiniz.

