---
title: Bakım sıraları
description: Bu konuda Varlık Yönetimi'ndeki bakım sıraları açıklanmaktadır.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 24f019547b9edc932c203d5dc8c73013007af599
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361054"
---
# <a name="maintenance-rounds"></a>Bakım sıraları

[!include [banner](../../includes/banner.md)]

 

**Varlık Yönetimi**'nde düzenli aralıklarla benzer bir görevi gerçekleştirmeniz gereken çeşitli varlıklar için bakım sıraları oluşturabilirsiniz. Örneğin aynı aralıklarda çeşitli makinelerde gerçekleştirilmesi gereken yağlama işleri veya güvenlik incelemesi işleri. İlk adım, aynı bakım işi formuna gereksinim duyan varlıklar dahil olmak üzere bir bakım sırası oluşturmaktır. Ardından, bakım sıralarını zamanlarsınız. Bakım sıralarını zamanlamayı tamamladığınızda sırayla ilgili tüm iş kayıtlarını **Tüm bakım zamanlaması** ve **Bakım zamanlaması satırları aç** seçeneklerinde görebilirsiniz.

>[!NOTE]
>Ayrıca sıraya dayalı iş emri oluştururken bakım sıraları, işlem yapılacak yerleşime yüklü varlıklarda tamamlanmak üzere işlem yapılacak yerleşimlerde ayarlanabilir. İşlem yapılacak yerleşimlerde bakım sıralarını ayarlama hakkında daha fazla bilgi için [İşlem yapılacak yerleşimler oluşturma](../functional-locations/create-functional-locations.md) bölümüne bakın.

## <a name="set-up-a-maintenance-round"></a>Bakım sırası ayarlama

1. **Varlık yönetimi** > **Kurulum** > **Önleyici bakım** > **Bakım sıraları**'na tıklayın.

2. Yeni bir bakım sırası oluşturmak için **Yeni**'ye tıklayın.

3. **Bakım sırası** alanına bir kod girin ve **Ad** alanına bakım sırası için bir ad girin.

4. **Başlangıç tarihi** alanında sıra için bir başlangıç tarihi seçin.

5. **Günler içinde bitirin** ve **Saatler içinde bitirin** alanlarına gün veya saat cinsinden beklenen bitiş tarihini ekleyebilirsiniz. Beklenen bitiş tarihi, bakım zamanlaması satırları oluşturulduğunda hesaplanan başlangıç tarihine göre hesaplanır. Örneğin ilgili işin başlangıç tarihinden itibaren bir hafta içinde tamamlanması gerektiğini belirtecek şekilde **Günler içinde bitir** alanına "7" ekleyebilirsiniz.

6. İş emirlerinin bu bakım sırasından oluşturulan bakım zamanlaması satırlarında otomatik olarak oluşturulması gerekiyorsa **Otomatik oluştur** geçiş düğmesinde "Evet"i seçin.

7. **İş emri türü** alanında, bu bakım sırasından oluşturulan iş emirlerinde kullanılacak iş emri türünü seçin.

8. **Hizmet düzeyi** alanında, bu bakım sırasından oluşturulan iş emirlerinde kullanılacak iş emri hizmet düzeyini seçin.

9. **Varlık satırları** hızlı sekmesinde, bakım sırasına varlık eklemek için **Ekle**'ye tıklayın.

10. Satır numarası, bakım sırasında varlıkların sırasını belirtecek şekilde **Satır numarası** alanına otomatik olarak girilir.

11. **Varlık** alanında varlığı seçin.

12. **Bakım işi türü** alanında varlık için bakım işi türünü seçin.

13. Gerekirse, bakım işi türüyle ilgili **Bakım işi türü çeşidi**'ni ve **Ticaret**'i seçin.

14. **Dönem türü** alanında yinelenmeyi (gün, hafta vb.) seçin.

15. **Dönem sıklığı** alanına bakım sırasının yinelenme sayısını girin. Örnek: **Dönem türü** alanında "Gün" seçeneğini belirlediyseniz ve bu alana "7" değerini girerseniz yeni bakım sırası satırları, önleyici bakım zamanlaması sırasında haftada bir kez oluşturulur.

16. **Başlangıç tarihi** alanında bakım sırasına dahil edilecek varlık için bir başlangıç tarihi seçin. Bu tarih, bakım sırasında ayarlanan başlangıç tarihinden farklı olabilir.

17. Bakım sırasına daha fazla varlık eklemek için 9-16. adımları tekrarlayın.

18. **İşlem yapılacak yerleşim satırları** hızlı sekmesinde, bakım sırasına işlem yapılacak yerleşim eklemek için **Ekle**'ye tıklayın. Yukarıdaki ilgili alanların açıklamasına bakın. Aynı alanlar, varlık satırı oluştururken de kullanılabilir ancak gerekirse işlem yapılacak yerleşim için **Üretici** ve **Model**'i de seçebilirsiniz. Bir satırda yalnızca işlem yapılacak yerleşimi seçerseniz ancak **Varlık türü**, **Üretici**, **Model**, **Bakım işi türü**, **Bakım işi türü çeşidi** ve **Ticaret** öğelerinde seçim yapmazsanız bakım zamanlaması sırasında bu işlem yapılacak yerleşimle ilgili tüm varlıklar bakım sırasına eklenir.

19. **Havuzlar** hızlı sekmesinde, bakım sırasına dahil edilecek bir iş emri havuzu seçmek için **Ekle**'ye tıklayın. Çeşitli iş emri havuzları tek bir bakım sırasına bağlanabilir.

20. Ayarınızı kaydedin.

>[!NOTE]
>**Başlık** hızlı sekmesindeki **Ayrıntılar** grubunda bulunan **Varlıklar** ve **Satırlar** alanları, seçilen bakım sırasıyla ilgili varlıkların ve satırların toplam sayısını gösterir.

Aşağıdaki çizimde üç varlığı içeren bir bakım sırası örneği gösterilmektedir.

![Şekil 1.](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a>Bakım sıralarını zamanla

Bakım sırasını ayarladığınızda bakım sırasıyla ilgili tüm işleri zamanlamak için bir iş zamanlaması çalıştırırsınız.

1. **Varlık yönetimi** > **Dönemsel** > **Önleyici bakım** > **Bakım sıraları zamanla** veya **Varlık yönetimi** > **Ortak** > **Bakım zamanlaması** > **Tüm bakım zamanlaması** veya **Bakım zamanlaması satırları aç** veya **Bakım zamanlaması havuzları aç**'a tıklayın > listeden bakım zamanlaması satırı seçin > **Bakım sıraları** düğmesine tıklayın.

2. **Dönem** alanında, işi zamanlamak için kullanılacak dönem türünü seçin.

3. **Dönem sıklığı** alanına, zamanlanan işe dahil edilecek dönem sayısını girin. Zamanlama başlangıcı geçerli tarihtir.

4. İş emrinin bakım sırasına göre otomatik olarak oluşturulması gerekiyorsa **Otomatik oluştur** geçiş düğmesinde "Evet"i seçin.

>[!NOTE]
>Bu geçiş düğmesi "Evet" olarak ayarlanırsa ve **Otomatik oluştur** geçiş düğmesi de **Bakım sıraları** formundaki bakım sırasında "Evet" olarak ayarlanırsa iş emirleri, bakım sırası satırları temel alınarak oluşturulur ve "Oluşturulan iş emri" durumuna sahip bakım zamanlaması satırları da oluşturulur. Yalnızca **Otomatik oluştur** geçiş düğmelerinden biri "Evet" olarak ayarlanırsa bu açılır menüde veya **Bakım sıraları**'nda, yalnızca "Oluşturuldu" durumuna sahip bakım zamanlaması satırları oluşturulur. Bu durumda, iş emri oluşturulmaz.

5. Gerekirse, işi zamanlamak için belirli sıralar veya başka bir başlangıç tarihi seçebilirsiniz. **Filtre**'ye tıklayın ve dahil edilecek sıraları ekleyin.

6. **Tamam**'a tıklayın.

7. Artık bakım sıraları işlerini **Varlık yönetimi** > **Ortak** > **Bakım zamanlaması** > **Tüm bakım zamanlaması** veya **Bakım zamanlaması satırları aç** seçeneklerinde görebilirsiniz. Zamanlanan sıralar, bir iş emri havuzuna bağlanırsa bakım zamanlaması satırlarını **Bakım zamanlaması havuzları aç** seçeneğinde de görebilirsiniz. Bir sıradan oluşturulan bakım zamanlaması satırları "Bakım sıraları" referans türüne sahiptir.

Aşağıdaki iki çizimde **Bakım sıralarını zamanla** iletişim kutusundaki bir zamanlama işi ve söz konusu zamanlama işine göre **Tüm bakım zamanlamaları**'nda oluşturulan bakım zamanlaması satırları gösterilmektedir.

![Şekil 2.](media/14-preventive-maintenance.png)

![Şekil 3.](media/15-preventive-maintenance.png)

- İş emirleri satıcı garantisi ile kapsanan varlıklarda el ile oluşturulduğunda kullanıcının garantiden haberdar olmasını sağlamak için bir iletişim kutusu gösterilir. İş emrinin oluşturulması daha sonra iptal edilebilir. Otomatik olarak oluşturulan iş emirleri için garanti ilişkisi denetimi atlanır.  
- Sıraları düzenli aralıklarla zamanlamak için **Arka planda çalıştır** hızlı sekmesinde bir toplu iş ayarlayabilirsiniz.  
- Sıra birkaç iş emri havuzuna dahil edilirse (bkz. [İş emri havuzları](../work-orders/work-order-pools.md)) bir kayıt her bir havuz için **Bakım zamanlaması havuzları aç** seçeneğinde gösterilir. Bu işlem, iş emri havuzlarının filtre seçeneklerini en iyi duruma getirmek için gerçekleştirilir.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]