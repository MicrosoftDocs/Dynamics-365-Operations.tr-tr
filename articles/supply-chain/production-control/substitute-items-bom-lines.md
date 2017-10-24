---
title: "Üretimde malzeme değiştirme"
description: "Bu konuda, üretim süreci sırasında malzemelerin nasıl değiştirileceği açıklamaktadır."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c98facf37659cc7039fc7f3057a530ceead5aa6a
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="material-substitution-in-manufacturing"></a>Üretimde malzeme değiştirme

[!include[banner](../includes/banner.md)]


Bu konuda, üretim süreci sırasında malzemelerin nasıl değiştirileceği açıklamaktadır. 

Üretim süreci sırasında malzemeleri değiştirmek için üç yöntem vardır:

-   Bir malzeme başka bir malzeme için belirli bir tarihten sonra değiştirildiğinde, tarihe göre
-   Bir formül içindeki malzeme, stok dışı olduğu için farklı bir malzeme ile değiştirildiğinde, master planlama sırasında
-   Bir malzeme beklenmedik şekilde stok dışı olduğunda ve farklı bir malzeme ile değiştirildiğinde, üretim sırasında

## <a name="substituting-material-by-date"></a>Tarihe göre malzeme değiştirme
Şu senaryoyu düşünün: Bir şirketin ürettiği makine, satıcı kataloğundan iki ay sonra kalkacak bir bileşen içeriyor. Bitiş tarihinden ileriye doğru satıcı eski bileşen yerine geçebilen yeni bir bileşen sunacak. İlk ve son geçerlilik tarihleri ürün reçetesi (BOM) satırlarında ayarlanabilir. Bu örnekte, **Bitiş tarihi** alanına bitiş tarihini girerek eski bileşenin sona ereceği tarihi ayarlayabilirsiniz. Ardından, ürün reçetesinde, yeni, değiştirme bileşeni eski bileşenin bitiş tarihinden sonra geçerli olacak şekilde ayarlayabilirsiniz. Bunu yapmak için, başlangıç tarihini **Başlangıç tarihi** alanına girin.

## <a name="substituting-material-by-planning"></a>Planlamaya göre malzeme değiştirme
Planlama sırasında malzemeleri bir ürün reçetesi kullanırken değil yalnızca formüller kullanırken değiştirebilirsiniz. Şu senaryoyu düşünün: Bir gıda üretim şirketi, 20 içerikli bir formülden sos yapıyor. Formüldeki bir içerik diğer iki içerikten biri yerine kullanılabiliyor. Ancak, bu iki içerik tercih edilen içerikten daha pahalı olduğundan, değiştirme yalnızca tercih edilen içerik stok dışı olduğunda kullanılıyor. Değiştirilebilen malzeme A olarak adlandırılırken, onun yerine kullanılabilecek iki malzeme B ve C olarak adlandırılır. Planlamaya göre malzeme değiştirme, formül satırlarındaki **Plan grubu** ve **Öncelik** alanları ile kontrol edilir. Bu örnekte, üç malzeme için formül satırları oluşturup formül satırlarını aynı plan grubu ile ilişkilendirin. Kurulumda, malzeme A için formül satırı en yüksek önceliğe (en düşük numaraya), malzeme C için formül satırı en düşük önceliğe ve malzeme B için formül satırı diğer iki satırın önceliği arasında bir önceliğe sahiptir. Tamamlanan madde için talebiniz varsa, master planlama, önce malzeme A için talebin karşılanabilirliğini belirler. Talep karşılanamıyorsa, master planlama öncelik sırasına göre malzeme B ve C'ye bakar. Malzeme B elde ise, formül için planlı toplu iş emri kesinleştikten sonra kullanılacaktır. Malzemelerin hiçbiri elde değilse, master planlama malzeme A için planlı iş emri oluşturur. **Not:** Bir plan grubunda formül satırları ayarlarken, yalnızca en yüksek önceliğe sahip malzemede miktar belirtmelisiniz. Bu miktar, malzemeler düşük önceliğe sahip olsa bile plandaki malzemelerin tümüne yönelik talebi hesaplamak için kullanılacaktır. Plan grubundaki düşük öncelikli maddelerde farklı miktarlar belirtemezsiniz.

## <a name="substituting-material-during-production"></a>Üretim sırasında malzeme değiştirme
Şu senaryoyu düşünün: Kaynak işlemi için bir parça metal levha gerekli. İşlem sırasında, ambar çalışanı, makine operatörünü levhanın stok dışı olduğu konusunda bilgilendirir. Ancak, levhanın biraz daha kalın bir levha ile değiştirilebileceğine karar verilir. Bu şekilde, işlem sonlandırılabilir. Bir açık üretim emri için ürün reçetesine malzeme eklenebilir. Üretim emri **Başlatıldı** durumunda ise, üretim ürün reçetesine yeni bir madde eklediklerinde kullanıcılardan emri yeniden tahmin etmeleri istenir. Malzeme eklendikten sonra, yeni madde için yeni bir malzeme çekme listesi oluşturulabilir. Yeni malzemeyi üretim ürün reçetesine eklemeniz gerekmez. Bunun yerine, doğrudan üretim malzeme çekme listesine ekleyebilirsiniz. Ardından, malzeme çekme listesini deftere nakledildiğinde, sistem malzemeyi üretim ürün reçetesine ekler.




