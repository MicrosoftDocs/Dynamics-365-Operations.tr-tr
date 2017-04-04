---
title: "Kuruluşlar ve kuruluş hiyerarşileri (ticaret essentials)"
description: "Ticaret essentials kuruluş taşıyan bir iş işlemini veya bir amaca ulaşmak amacıyla tanımlayabilirsiniz iç kuruluşların üç tür vardır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21251
ms.assetid: 2bfc6bfe-784b-42e8-8bf0-116e9f0a558e
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 93711977ad8d861ca75ba80ee542ee112c8ddd2f
ms.lasthandoff: 03/31/2017


---

# <a name="organizations-and-organizational-hierarchies-commerce-essentials"></a>Kuruluşlar ve kuruluş hiyerarşileri (ticaret essentials)

Ticaret essentials kuruluş taşıyan bir iş işlemini veya bir amaca ulaşmak amacıyla tanımlayabilirsiniz iç kuruluşların üç tür vardır. 

Bir organizasyon, bir iş sürecini gerçekleştirmek veya bir hedefe ulaşmak için birlikte çalışan bir grup insandır. Bir organizasyon hiyerarşisi, organizasyonunuzu meydana getiren ticari birimler arasındaki ilişkileri temsil eder.

## <a name="organizations"></a>Kuruluşlar
Ticaretle ilgili temel bilgileri altında şu dahili organizasyon türlerini tanımlayabilirsiniz: tüzel kişilikler, işletme birimleri ve ekipler. Microsoft Dynamics AX'te tüm dahili organizasyonlar Taraf kuruluş türündedir. Bu nedenle, bu organizasyonlar adres ve diğer iletişim bilgilerini depolamak için bir adres defteri kullanır. Taraflar bir kişi veya organizasyon olabilir ve bir veya daha fazla sayıda adres defterine ait olabilir.
### <a name="legal-entities"></a>Tüzel kişilikler

Tüzel kişilik, kayıtlı veya asal bir yapıya sahip olan bir organizasyondur. Tüzel kişilikler yasal sözleşmelere girebilir ve performanslarını raporlayacak bildirimler hazırlamaları gerekir. Şirket, Microsoft Dynamics AX'teki bir tüzel kişilik türüdür ve her tüzel kişilik bir şirket numarasıyla ilişkilidir. Bu ilişki şirket kimliğinin veya DataAreaId'in, şirketlerin veri güvenliği için bir sınır olarak kullanıldığı bazı veri modellerinde kullanılmasından kaynaklanmaktadır. Kullanıcılar, yalnızca oturum açmış oldukları şirketin verilerine erişebilir.

### <a name="operating-units"></a>İşletme birimleri

Bir işletme birimi bir işletmenin ekonomik kaynaklarının ve yönetimsel işlemlerinin kontrolünü bölmek için kullanılan bir kuruluştur. Bir işletme birimindeki kişiler az bulunur kaynakların kullanımını en üst düzeye çıkarmak, süreçleri geliştirmek ve performansları için hesap verme görevlerine sahiptirler. Ticaretle ilgili temel bilgileri altında, işletme birimleri türleri maliyet merkezlerini, iş birimlerini, değer akışlarını, departmanları ve perakende kanallarını içerir. Aşağıdaki tabloda her bir işletme birimi türü hakkında daha fazla bilgi bulabilirsiniz.
|                         |                                                                                         |                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Faaliyet birimi türü** | **Açıklama**                                                                         | **Amaç**                                                                                                                                 |
| İş birimi           | Stratejik iş hedeflerini karşılamak için oluşturulan yarı özerk bir işletme birimi. | İşletme birimlerini organizasyonun tüzel kişiliklere hizmet sunduğu endüstrilere veya ürün serilerine dayalı finansal raporlama için kullanın. |
| Perakende kanalı          | Bir işletme birimi bir fiziksel mağazayı temsil etmektedir.                             | Tüzel kişilikler içinde veya arasında bir veya daha fazla mağazayı yönetmek ve kontrol etmek için kullanın.                                                               |

## <a name="organizational-hierarchies"></a>Organizasyonel hiyerarşiler
Ticaretle ilgili temel bilgileri altında her bir hiyerarşiye bir amaç atanır. Bir hiyerarşinin amacı, hiyerarşiye dahil edilebilecek organizasyon türlerini belirlemektir. Amaç ayrıca bir hiyerarşinin hangi uygulama senaryolarında kullanılabileceğini de belirler. Örneğin, perakende hiyerarşisi perakende satış mağazasında ürünleri satmak ve satın almak için kullanılabilir. Bir hiyerarşi içindeki kuruluşlar parametreleri, politikaları ve hareketleri paylaşabilir. Bir organizasyon, ana organizasyonun parametrelerini devralabilir veya bu parametreleri değiştirebilir. Ancak, ürünler ve adres defterleri gibi paylaşılan master veriler tüm organizasyon için geçerlidir ve tek tek organizasyonlar tarafından değiştirilemez.
### <a name="best-practices-for-setting-up-an-organization-in-a-hierarchy"></a>bir hiyerarşi içinde bir kuruluş oluşturulması için en iyi uygulamalar

Bir organizasyon hiyerarşisi uygularken aşağıdaki en iyi uygulamaları dikkate alın:
-   Bir tüzel kişilik ile bir ticari birim arasındaki kesişimi belirtmek için bir departman oluşturun. Ardından, yasal raporlama işlemi için verileri bir departmandan tüzel kişiliğe ve dahili raporlama için bir departmandan bir ticari birime aktarabilirsiniz.
-   Tek bir tüzel kişilik içinde, aynı hiyerarşi amacı için birden fazla hiyerarşi oluşturmayın.
-   Her amaç için bir hiyerarşi oluşturmayın. Genellikle, bir hiyerarşiyi birden faza amaç için kullanabilirsiniz. Örneğin, bir işletme birimleri hiyerarşisi, politikayla bağlantılı tüm amaçlara atanabilir.
-   Dengeli hiyerarşiler oluşturun. Bir hiyerarşide kök düğümü ile aynı uzaklıkta bulunan tüm düğümler bir düzey olarak tanımlanır. Dengeli bir hiyerarşi içinde, her düzeyde yalnızca bir işletme birimi türü oluşabilir ve kök düğümün her bir düzeye olan uzaklığı aynıdır. Bir departman ile bir tüzel kişilik veya bir ticari birim arasında ara düzeyler varsa, dengeli bir hiyerarşinin oluşturulması için yer tutucu organizasyonlar gerekebilir.
-   Tüzel kişilikler için yapı aynı zamanda işletim yapınız ise ayrı bir işletme birimleri hiyerarşisi oluşturmayın. Tüzel kişilikler ve işletme birimleri içeren karışık bir hiyerarşi her iki amaca da hizmet eder.
-   Temel yeniden yapılandırma senaryoları oluşturmadan önce bir etki analiz ve bir doğrulama testi gerçekleştirmek için hiyerarşinin geçerlilik tarihlerini kullanın.
-   Bir hiyerarşi yayımlamadan önce değiştirme ihtimaliniz varsa bu hiyerarşiyi taslak olarak kaydedin.
-   Bir üretim ortamındaki bir hiyerarşiye organizasyon etkilemeye veya bu hiyerarşiden organizasyon çıkarmaya yetkili kişi sayısını sınırlandırın. Bu sayının sınırlandırılması, maliyetli hataların yapılması ihtimalini ve düzeltme ihtiyacını azaltacaktır.

## <a name="retail-store-management"></a>Perakende mağazası yönetimi
Aşağıdaki tabloda, organizasyon hiyerarşilerinin kullanılabildiği Ticaretle ilgili temel bilgiler senaryoları açıklanmıştır.
| Görev                                                                           | Açıklama                                                                                                                                                                                                                                                                                                | Hiyerarşinin amacı    |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Perakende ürün çeşitlerini yönetme                                                      | Her bir perakende mağazasında bulunan ürünleri tanımlayın.                                                                                                                                                                                                                                             | Perakende ürün çeşidi    |
| Perakende stok yenilemesini yönetme                                                    | Stok yenileme kurallarına dayalı olarak stok yenilemesi için mağazaları gruplandırın.                                                                                                                                                                                                                                          | Perakende stok yenilemesi |
| Mağazalar için veri raporlama                                                         | Raporlama için mağazaları gruplandırın.                                                                                                                                                                                                                                                                                | Perakende raporlaması     |
| Stok nakledin, bildirimleri hesaplayın ve bir mağaza grubu için bildirimleri nakledin | Bir toplu iş için atanabilecek bir mağaza grubu oluşturun. Stok nakletmek, bildirim hesaplamak veya bildirim nakletmek üzere bir toplu iş tanımladığınıza işin hangi hiyerarşi için uygulanacağını seçebilirsiniz. Mağazalar hiyerarşiye eklendiğinde veya hiyerarşiden çıkarıldığında toplu işi değiştirmenize gerek olmaz. | Retail POS nakli   |




