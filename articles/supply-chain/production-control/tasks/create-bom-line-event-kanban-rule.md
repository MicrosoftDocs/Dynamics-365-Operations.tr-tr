---
title: Ürün reçetesi satırı olayı kanban kuralı oluşturma
description: Bu görev, karışık bir yalın ve klasik üretim ortamında üretim BOM hatları için tedarikin garanti edilmesi amacıyla bir olay kanban kuralının oluşturulması için gerekli kurulum üzerine odaklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcef749139635b2d8858a85154ff7619c16857d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998765"
---
# <a name="create-a-bom-line-event-kanban-rule"></a>Ürün reçetesi satırı olayı kanban kuralı oluşturma

[!include [banner](../../includes/banner.md)]

Bu görev, karışık bir yalın ve klasik üretim ortamında üretim BOM hatları için tedarikin garanti edilmesi amacıyla bir olay kanban kuralının oluşturulması için gerekli kurulum üzerine odaklanmaktadır. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu görev, yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.


## <a name="create-a-new-kanban-rule"></a>Yeni bir kanban kuralı oluştur
1. Üretim denetimi > Periyodik görevler > Kanban miktarı hesaplama > Kanban kuralları öğesine gidin.
2. Yeni'ye tıklayın.
3. Tür alanından 'Çek' seçimini yapın.
    * Çekme türü, transfer kanbanlarının oluşturulması için kullanılır.  
4. Yenileme stratejisi alanında 'Olay' öğesini seçin.
    * Olay stratejisi, bir olaya göre kanbanların transferinin oluşturulması için seçilir. Görev kılavuzunda daha sonra bunu bir üretim emri tahmin ederek tetikleyeceğiz.  
5. İlk plan alanında bir değer girin veya bir değer seçin.
    * ReplenishSpeakerComponents öğesini girin veya seçin. Bu transfer faaliyeti, alıcı (çıkış) ambarına ve konum 12'ye sahiptir, bu da malzemenin ambar 12'deki konum 12'ye taşınacağı anlamına gelir.  
6. Ayrıntılar bölümünü genişletin.
7. Üretim alanına M0001 değerini girin veya buradan M0001 değerini seçin.
8. Olaylat bölümünü genişletin.
9. BOM satır olayı alanında 'Otomatik' öğesini seçin.
    * BOM satır olayı alanı Otomatik olarak ayarlandıktan sonra, üretim emri BOM satırları için malzeme ihtiyaçlarını karşılamak üzere kanban oluşturulur.  
10. Sayfayı kapatın.

## <a name="create-and-modify-a-new-production-order"></a>Yeni üretim emri oluşturma ve değiştirme
1. Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.
2. Yeni üretim emri'ne tıklayın.
3. Madde numarası alanında bir değer girin veya seçin.
    * 'L0001' öğesini girin veya seçin. M0001, madde L0001 için BOM'a dahil edileceğinden L0001 maddesini kullanıyoruz.  
4. Oluştur'a tıklayın.
5. Listede, L0001 sırasındaki bağlantıya tıklayın.
6. Ürün reçetesine tıklayın.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Düzenle öğesine tıklayın.
9. Satır türü alanından 'İlişkilendirilen tedarik' öğesini seçin.
    * Bir kanban tedariki oluşturma sürecinin tetiklenmesi için ilişkilendirilmiş tedarik kullanılır.  
10. Kaynak tüketimi alanında Hayır'ı seçin.
    * Kaynak tüketimi onay kutusundaki işaret kaldırıldığında ambar değiştirilebilir.  
11. Stok boyutları bölümünü genişletin.
12. Ambar alanına '12' yazın.
    * Çekme faaliyeti için çıkış ambarı olduğundan ambar, 12 olarak ayarlanır.  
13. Konum alanına '12' yazın.
    * Çekme faaliyeti için çıkış konumu olduğundan konum, 12 olarak ayarlanır.  
14. Sayfayı kapatın.
15. Sayfayı kapatın.

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>Üretim emrini tahin etme ve oluşturulan kanbanı görüntüleme
1. Tahmin seçeneğine tıklayın.
    * Üretim emrinin tahmin edilmesi, ilişkili kanbanın M0001 tedarik maddesine oluşturulması tetiklenir.  
2. Tamam'a tıklayın.
3. Sayfayı kapatın.
4. Sayfayı kapatın.
5. Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.
6. Listede, seçili satırdaki bağlantıya tıklayın.
    * Madde M0001 için oluşturulan olay kanban kuralını seçin.  
7. Kanbanlar bölümünü genişletin.
8. Listede, seçili satırı işaretleyin.
    * Kanbanın, tahmini üretim emri için M0001 tedarik edilmesi amacıyla oluşturulduğuna dikkat edin.  
    * Bu son adımdır!  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]