--- 
title: "Dalga işlemeyi yapılandırma"
description: "Bu kılavuz bir dalga işlendiğinde bir ambar için hangi işin oluşturulacağını belirlemek için ölçütleri ayarlamayı ve dalgaların manuel mi yoksa otomatik olarak mı işlemden geçirileceğini açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 50988c689995dbb957af760c9c2c3b823f557c86
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="configure-wave-processing"></a>Dalga işlemeyi yapılandırma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu kılavuz bir dalga işlendiğinde bir ambar için hangi işin oluşturulacağını belirlemek için ölçütleri ayarlamayı ve dalgaların manuel mi yoksa otomatik olarak mı işlemden geçirileceğini açıklar. Ölçütleri, bir dalgayı yayımlanan satış siparişleri, üretim emirleri veya kanban siparişleri ile eşleştiren dalga şablonları ve sorguları oluşturarak belirtebilirsiniz. Dalga işleme, Ambar yönetim modülünde bu işlevi kullanan ambarlarda kullanılır, Stok yönetim modülünde bu işlevi kullananlarda kullanılmaz. Bu yordamı USMF demo veri şirketinde çalıştırabilirsiniz.

1. Ambar yönetimi > Kurulum > Dalgalar > Dalga şablonları öğesine gidin.
2. Yeni'ye tıklayın.
3. Dalga şablonu adı alanına bir değer girin.
    * Bir dalga şablonu oluştururken, şablonların hangi sırada eşleneceğini ve satış siparişlerine, üretim emirlerine veya kanbanlara yayınlanacağını belirtirsiniz. Bir satır ambar veya üretim için serbest bırakıldığında ölçütlerini karşılayan ilk dalga şablonunu kullanır. Listenin üstündeki en belirgin ölçütlerle sahip şablonları koymanızı öneririz. Ölçüt ne kadar geniş olursa, bir satırın ölçüte uyması o kadar yüksek olasılığa sahip olur ve bu da satırların yanlış dalgaya atanmasına sebep olabilir.  
4. Dalga şablonu açıklaması alanında bir değer girin.
5. Tesis alanına bir değer girin veya buradan bir değer seçin.
    * USMF kullanıyorsanız, site 2'yi seçebilirsiniz.  
6. Ambar alanında bir değer girin veya bir değer seçin.
    * USMF kullanıyorsanız, ambar 24'ü seçebilirsiniz.  
7. Otomatik dalga oluşturma alanını Evet olarak ayarlayın.
    * Bir satış emri, üretim emri veya kanban serbest bırakıldığında otomatik olarak dalga oluşturmak için bu seçeneği belirleyin.  
8. Dalga yayın ambar işleme seçeneğini Evet olarak ayarlayın. 
    * Satır ambara serbest bırakıldığında otomatik olarak dalgayı işlemek ve iş oluşturmak için bu seçeneği belirleyin.  
9. Otomatik dalga yayımlama seçeneğini Evet olarak ayarlayın. 
    * Dalgayı otomatik olarak serbest bırakmak için bu seçeneği belirleyin. Malzeme çekme işi oluşturulur ve mobil cihazlarda kullanılabilir.  
10. Açık dalgalara ata seçeneğini Evet olarak ayarlayın. 
    * Satırlar, dalgalara, dalga şablonu için sorgu filtresi temel alınarak atanır.  
11. Dalgayı eşikte otomatik işle seçeneğini Evet olarak ayarlayın. 
    * Dalganın değerleri Dalga eşikleri alan grubunda belirtilen ağırlık, sevkıyat ve satır eşiklerine eriştiğinde dalgayı otomatik olarak işlemek için bu seçeneği belirleyin. Bu seçenek yalnızca, Dalga şablon türü alanında Sevkıyat seçilirse kullanılabilir.  
12. Otomatik stok yenileme işi yayımla seçeneğini Evet olarak ayarlayın. 
    * Talep tabanlı stok yenileme işi oluşturmak ve bunu otomatik olarak serbest bırakmak için bu seçeneği belirleyin. Stok yenileme dalga yöntemini dalga şablonuna eklemeniz Dalga talebi türünde stok yenileme şablonu oluşturmanız gerekir.  
13. Yöntemler bölümünü genişletin.
    * Dalga şablonu yöntemleri, her bir dalganın işlendiğinde geçirileceği etkinlikler dizisini denetlemenize olanak sağlar. Örneğin, dalga stok yenilemesi için bir yönteme sahip olabilirsiniz. Bir yöntem eklediğinizde, adımlar sırasında otomatik olarak uygun konumda listelenir. Otomatik stok yenileme işi yayın seçeneğini Evet olarak ayarladıysanız, yenileme yöntemini buraya eklemeniz gerekir.  
    * Dalga öznitelikleri, dalgayı kullanabilecek öğelerin türünü sınırlamak için filtreler olarak çalışır. Örneğin, bir madde grubu belirtebilirsiniz.  
14. Kaydet'e tıklayın.
15. Sayfayı kapatın.
16. Ambar yönetimi > Kurulum > Ambar yönetimi parametreleri öğesine gidin.
17. Dalga işleme bölümünü genişletin.
18. Dalga işleme toplu iş grubu alanında bir değer girin veya seçin.
19. Dalgaları toplu iş olarak işle seçeneğini Evet olarak ayarlayın.
20. Kilit için bekle (ms) alanında, bir sayı girin.
    * Tahsisat adımının, başka bir tahsisat kaynağı tarafından kilitlenmiş olan bir sistem kaynağı için bekleyeceği zamanı, milisaniye cinsinden girin. Bu süre aşıldığında, dalga işlenmez ve bir hata iletisi görüntülenir.  
21. Kaydet'e tıklayın.
22. Sayfayı kapatın.
23. Üretim denetimi > Kurulum > Üretim denetimi parametreleri öğesine gidin.
24. Ambara yayınla alanında, bir seçenek belirleyin.
    * Satış siparişleri ve kanban siparişleri için, sipariş için ambarda serbest bırakılmadan önce stok ayrılmalıdır. Aksi halde, maddeler veya tahsisat satırları dalga içerisinde işlenemez. Üretim emirleri için Kısmi rezervasyona izin ver'i seçme seçeneğiniz de vardır. Örneğin, üretimi başlatmak için gereken malzemeler varsa ve daha sonra işlemin bitirilmesi için ek malzemelerin kullanılabilir olmasını bekleyebiliyorsanız. Bu seçeneği belirlerseniz, ek malzemeler kullanılabilir duruma geldiğinde, ambara serbest bırak işlemini el ile tekrar etmeniz gerekir.  
25. Sayfayı kapatın.

