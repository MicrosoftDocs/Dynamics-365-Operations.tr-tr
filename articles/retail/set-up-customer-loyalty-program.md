---
title: "Müşteri bağlılık programı ayarlama"
description: "Bu makalede bir bağlılık programının nasıl oluşturulacağı açıklamaktadır. Bağlılık programları, müşterileri perakende mağazalarınızdan ürün satın aldığı için ödüllendirerek müşteri bağlılığını artırmanıza yardımcı olabilir. Microsoft Dynamics 365 for Retail'de, herhangi bir perakende kanalındaki tüzel kişiliklerinize uygulanan basit veya karmaşık bağlılık programları ayarlayabilirsiniz."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 710f8ae3a6a2b5072f37879aad066dc699ede8f0
ms.contentlocale: tr-tr
ms.lasthandoff: 06/20/2017

---

# <a name="set-up-a-customer-loyalty-program"></a>Müşteri bağlılık programı ayarlama

[!include[banner](includes/banner.md)]


Bu makalede bir bağlılık programının nasıl oluşturulacağı açıklamaktadır. Bağlılık programları, müşterileri perakende mağazalarınızdan ürün satın aldığı için ödüllendirerek müşteri bağlılığını artırmanıza yardımcı olabilir. Microsoft Dynamics 365 for Retail'de, herhangi bir perakende kanalındaki tüzel kişiliklerinize uygulanan basit veya karmaşık bağlılık programları ayarlayabilirsiniz.

<a name="loyalty-features"></a>Bağlılık programı özellikleri
----------------

Aşağıdaki seçenekleri içeren bir bağlılık programı ayarlayabilirsiniz:

-   Bağlılık programlarınızda sunduğunuz birden çok ödül türünü ayarlayın ve bağlılık programlarına katılımı izleyin.
-   Sunduğunuz farklı ödül teşviklerini temsil eden bağlılık programları ayarlayın. Daha sık alışveriş yapan veya mağazalarda daha fazla para harcayan müşterilere daha büyük teşvikler ve ödüller sunmak için bağlılık programı katmanları ekleyin.
-   Bir müşterinin ödülleri kazanması için tamamlaması gereken etkinlikleri tanımlamak üzere kazanç kuralları tanımlayın. Ayrıca, bir müşterinin ödülleri ne zaman ve nasıl kullanabileceğini belirleyen kullanım kuralları da tanımlayabilirsiniz.
-   Bağlılık programlarınıza katılan herhangi bir perakende kanalından bağlılık kartları çıkarın ve bağlılık kartlarını, müşterinin katılabileceği bir veya daha fazla bağlılık programına bağlayın. Ayrıca müşteri kaydını bir bağlılık kartına bağlayarak müşterinin birden fazla karttan bağlılık puanları toplayıp kullanabilmesini de sağlayabilirsiniz.
-   Bağlılık programı kartlarını el ile ayarlayın ya da bir müşteriyi ödüllendirmek veya ihtiyacını karşılamak için bağlılık ödülleri bakiyesini bir karttan diğerine transfer edin.

## <a name="setting-up-loyalty-programs"></a>Bağlılık programları ayarlama
Dynamics 365 for Retail'de bağlılık özelliğini etkinleştirmek için çeşitli bileşenleri ayarlamanız gerekir. Aşağıdaki diyagram, bağlılık bileşenlerini ve birbirleriyle ilişkisini gösterir. ![Bağlılık programı ayarlama işlem akışı](./media/loyaltyprocess.gif)

## <a name="loyalty-components"></a>Bağlılık programı bileşenleri
Aşağıdaki tabloda her bir bileşen ve bağlılık programı ayarlarında nerede kullanıldığı tanımlanmıştır.

| Bileşen                                        | Açıklama                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Kullanıldığı yer                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| İskontoları ayarlama (önkoşul)                  | Bağlılık programı müşterilerinize sunduğunuz iskontoları ayarlayın. Örneğin, tüm giyim ürünlerinde yüzde 5 indirim sunabilirsiniz.                                                                                                                                                                                                                                                                                                                                                                                                                                                            | İskontolar, fiyat grupları bir bağlılık programına dahil edilmeden önce eklenmelidir. Fiyat grupları, bağlılık programlarına ve bağlılık programı katmanlarına atanır.                                                                                                                                                                                                                      |
| Fiyat gruplarını ayarlama (önkoşul)               | Fiyat grupları, perakende ürünler için fiyatları ve iskontoları oluşturmak ve yönetmek için kullanılır. Bağlılık programlarınıza uygulanan iskontoları içeren fiyat gruplarını ayarlayın.                                                                                                                                                                                                                                                                                                                                                                                                             | Fiyat grupları, bağlılık programlarına ve bağlılık programı katmanlarına atanır.                                                                                                                                                                                                                                                                                                        |
| Kanalları ayarlama (önkoşul)                   | Perakende kanalları, bir adreste hizmet veren mağaza, çevrimiçi mağaza veya çağrı merkezi gibi bağlılık programlarınıza katılan mağazalardır. Bunlara bağlılık programları atamadan önce perakende kanallarınızı ayarlamanız gerekir.                                                                                                                                                                                                                                                                                                                                                      | Perakende kanalı bağlılık programına katılıyorsa ilgili perakende kanalını bağlılık programına atarsanız.                                                                                                                                                                                                                                                                  |
| Bağlılık programı ödeme yöntemi ayarlama (önkoşul) | Bir bağlılık programı kartının bir kayıtta kullanılabilmesi için bir ödeme yöntemi ayarlamanız gerekir, bağlılık programı puanları bir bağlılık programı kapsamında kullanılabilir. Müşterilerin bağlılık programı puanlarını ürünlerde kullanabilmesi için perakende kanalına bağlılık programı ödeme yöntemi de eklemeniz gerekir.                                                                                                                                                                                                                                                                                           | Bir bağlılık programı türü ödeme yöntemi ayarlayın, sonra bağlılık programı ödeme yöntemini bağlılık programına katılan perakende kanallarına atayın.                                                                                                                                                                                                                          |
| Tarih aralıklarını ayarlama                            | Tarih aralıkları, bağlılık programı katmanları için geçerli zaman aralığını ayarlamanın esnek bir yolunu sağlar. Bir müşterinin bir katmanında ne kadar kalacağını veya bir katman için uygun hale gelmesi için bir etkinliği ne kadar sürede tamamlaması gerektiğini belirlemek için tarih aralıklarını kullanın.                                                                                                                                                                                                                                                                                                                                            | Tarih aralıkları yalnızca bağlılık programlarınızda katmanlar kullanıyorsanız geçerlidir. Program katmanlarında geçerli tarih aralığını ve program katmanı kuralları için geçerli tarih aralıklarını seçin.                                                                                                                                                                                  |
| Ödül puanlarını ayarlama                             | Ödül puanları, müşterilerinize sunduğunuz ödül türleridir. Ödül puanları, kullanılabilir veya kullanılamaz özelliktedir. Kullanılabilir ödül puanları ürünlerle takas edilebilir. Kullanılamaz ödül puanları, izleme amaçlarıyla veya bağlılık programındaki bir müşteriyi sonraki katmana ilerletmek için kullanılır.                                                                                                                                                                                                                                                                          | Ödül puanları, katman kurallarında gösterilir ve bir müşterinin belirli bir katman için uygunluğunu belirlemek üzere kullanılır. Ödül puanları, bağlılık programı planlarında kazanç ve kullanım kurallarında da gösterilir. Kazanç kurallarında, müşterinin belirli bir etkinlik neticesinde kazanabileceği ödülleri belirtirsiniz. Kullanım kurallarında, müşterinin kullanabileceği ödülü belirtirsiniz.                  |
| Bağlılık programları ayarlama                          | Bağlılık programları, sunduğunuz temel bağlılık öğeleridir. Her bir bağlılık programına atanmış bağlılık programı katmanları vardır. İskontolar ve fiyat grupları, program düzeyinde ya da katman düzeyinde bağlılık programlarına atanır.                                                                                                                                                                                                                                                                                                                                             | Bağlılık programlarınız için bağlılık programı planları oluşturursunuz. Bağlılık programı kartlarını bağlılık programlarınıza atarsınız ve sonra bu kartlar müşterilere atanabilir. Perakende kanalları, bağlılık programı planlarına atanmış olan bağlılık programları katılır. Bağlılık programı kartına sahip tüm müşteriler ilgili karta atanmış bağlılık programlarına katılabilir.            |
| Bağlılık programı katmanları ve katman kuralları ayarlama              | Bağlılık katmanları, bağlılık programlarınız için tanımlayabileceğiniz isteğe bağlı düzeylerdir. Bağlılık programına katılan tüm müşteriler için taban fiyat iskontolarının ve ödüllerin yanı sıra, program içinde çeşitli düzeylere ulaşan müşteriler için ek iskontolar ve ödüller de ayarlayabilirsiniz. Tanımladığınız her bir bağlılık programı katmanına yönelik olarak o katmana uygun bir müşteri için kurallar ayarlayabilirsiniz. O katmana ulaştıktan sonra müşterilerin orada ne kadar süreyle kalabileceğini de belirleyebilirsiniz.                                                                                  | Bağlılık programı katmanları ve bağlılık programı katman kuralları bağlılık programları içinde tanımlanır. Hiçbir bağlılık programı katmanı tanımlamazsanız, bağlılık programına katılan tüm müşteriler bağlılık programı fiyat grubunu atadığınız iskontolar için uygun olur. Bağlılık programı katmanları tanımlarsanız, bağlılık programı planındaki bağlılık programları katmanları için kazanç ve kullanım kuralları ayarlayabilirsiniz. |
| Bağlılık programı planları kurma                           | Bağlılık programı planları, seçilen bağlılık programı için geçerli kullanım ve kazanç kurallarını belirtir. Bağlılık programını, kazanç kurallarını ve bir perakende mağaza için geçerli kullanım kurallarını tanımlamak için bir bağlılı programı planına perakende kanalları atarsınız.                                                                                                                                                                                                                                                                                                                                  | Bir bağlılık programı planı, bağlılık programına ve perakende kanallarına atanır. Birden çok bağlılık programı planını aynı bağlılık programına veya çok sayıda perakende kanalına atayabilirsiniz.                                                                                                                                                                        |
| Bağlılık programı kartları ayarlama                             | Bir bağlılık programı kartı, kart sahibine ilgili karta atanmış bağlılık programlarına katılma yetkisi verir. Bağlılık programı kartları anonim olarak verilebilir ya da belirli bir müşteriye atanabilir. Belirli bir kart için bağlılık programı hareketlerini ve kartta birikmiş bağlılık programı puanlarına yönelik özeti görüntüleyebilirsiniz. Herhangi bir perakende kanalından bağlılık programı kartları verebilirsiniz. Müşteriyi farklı bir katmana yükseltmek, bağlılık programı puanı eklemek veya bağlılık programı puan bakiyesini bir karttan diğerine aktarmak için bir bağlılık programı kartını el ile de ayarlayabilirsiniz. | Bağlılık programlarını bir bağlılık programı kartına atarsınız.                                                                                                                                                                                                                                                                                                                                  |

## <a name="loyalty-processes"></a>Bağlılık programı işlemleri
Aşağıdaki tabloda, bağlılık programı yapılandırmaları ile verilerini mağazalarınıza göndermek ve mağazalarınızdan bağlılık programı hareketlerini almak için çalıştırılması gereken işlemler açıklanır.

| İşlem adı                         | Açıklama                                                                                                                                                                                                                                                                                                                                                                                                    | Sayfa adı                            |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| 1050 (bağlılık programı bilgileri)           | Bağlılık programı verilerini Microsoft Dynamics 365 for Retail'den perakende mağazalarına göndermek için bu işlemi çalıştırın. Bağlılık programı verilerinin tüm mağazalara aktarılabilmesi için bu işlemi sık çalışacak şekilde zamanlamak iyi bir fikirdir.                                                                                                                                                                                               | Dağıtım planı                |
| Bağlılık şemalarını işle              | Bağlılık programı planlarını bağlılık programı planının atandığı perakende kanallarıyla ilişkilendirmek için bu işlemi çalıştırın. Bu işlem, toplu işlem olarak çalışacak şekilde zamanlanabilir. Bağlılık programı planları, bağlılık programları veya bağlılık programı ödül puanları gibi bağlılık programı yapılandırma verilerini değiştirirseniz bu işlemi çalıştırmanız gerekir.                                                                                               | Bağlılık şemalarını işle              |
| Çevrimdışı bağlılık programı hareketlerini işle | Çevrimdışı işlenen hareketlerin bağlılık programı kartlarına dahil edilebilmesi amacıyla bu kartları güncellemek için bu işlemi çalıştırın. Bu işlem yalnızca **Paylaşılan perakende parametreleri** sayfasında **Çevrimdışı kazan** onay kutusu işaretlendiğinde geçerlidir, böylece ödüller çevrimdışıyken kazanılabilir.                                                                                                                                               | Çevrimdışı bağlılık programı hareketlerini işle |
| Bağlılık programı kartı katmanlarını güncelle            | Müşterinin kazanç etkinliğini bir bağlılık programının katman kurallarına göre değerlendirmek ve müşterinin katman durumunu güncelleştirmek için bu işlemi çalıştırın. Bu işlem yalnızca bağlılık programlarındaki katman kurallarını değiştirmek ve güncel kuralların önceden verilmiş bağlılık programı kartları için geriye dönük olarak geçerli olmasını istiyorsanız gereklidir. Bu işlem, toplu bir şeklinde veya tek tek kartlar için çalıştırılabilir. | Bağlılık programı kartı katmanlarını güncelle            |





