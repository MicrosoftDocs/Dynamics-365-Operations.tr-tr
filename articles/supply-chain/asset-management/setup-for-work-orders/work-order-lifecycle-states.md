---
title: İş emri yaşam döngüsü durumları
description: Bu konuda Kıymet Yönetimi'nde iş emri yaşam döngüsü durumunu açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderLifecycleState, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6e96f2f6b324ffe44e8684d9bd2a42fb52d0aed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439353"
---
# <a name="work-order-lifecycle-states"></a>İş emri yaşam döngüsü durumları


[!include [banner](../../includes/banner.md)]

 

İş emri yaşam döngüsü durumları bir iş emrinin gidebileceği durumları tanımlar. Örnekler **Oluşturulan**, **Planlanan**, **İşlemde** ve **Bitti**'yi içerir. İş emri yaşam döngüsü durumları bir iş emrinde el ile güncelleştirilebilir veya otomatik olarak güncelleştirilebilir (örneğin, iş emri planlaması sırasında).

İş emirleriniz için gerekli olan iş emri yaşam döngüsü durumları, **Ğroje yönetimi ve muhasebe parametreleri** sayfasındaki eşleşen proje aşamalarına iliştirilmesi gerekir (**Proje yönetimi ve muhasebe** \> **Proje yönetimi ve muhasebe parametreleri**). Proje aşamalarını önce proje yönetimi ve muhasebede ayarlarsınız. Daha sonra, iş emri yaşam döngüsü durumlarını ve iş emri yaşam döngüsü modellerini kıymet yönetiminde ayarlarsınız.

Aşağıdaki tablo **İş emri yaşam döngüsü durumları** sayfasının **Genel** hızlı sekmesindeki **İş emri** ve **Plan** bölümlerini açıklar(**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Yaşam döngüsü durumları**).

![İş emri yaşam döngüsü durumu sayfası](media/09-setup-for-work-orders.png)

| Seçenek adı                   | Tanım |
|-------------------------------|-------------|
| Active                        | İş emrinin bu yaşam döngüsü durumundayken etkin olması gerekiyorsa bu seçeneği **Evet** olarak ayarlayın. |
| Satır ekle                      | İş emri işleri bu yaşam döngüsü durumunda olan bir iş emrine eklenebilecekse bu seçeneği **Evet** olarak ayarlayın. |
| Sil                        | İş emrinin bu yaşam döngüsü durumundayken siliniyor olması gerekiyorsa bu seçeneği **Evet** olarak ayarlayın. |
| Satırı sil                   | İş emri işleri bu yaşam döngüsü durumunda olan bir iş emrinden silinebilecekse bu seçeneği **Evet** olarak ayarlayın. |
| Planlamaya izin ver              | İş emrinin bu yaşam döngüsü durumundayken planlanan olması gerekiyorsa bu seçeneği **Evet** olarak ayarlayın. |
| Fiili başlangıcı ayarla              | Bu yaşam döngüsü durumuna güncelleştirildiğinde, kullanıcıdan iş emri için gerçek başlangıç tarihi ve saati seçmesi istenirse bu seçeneği **Evet** olarak ayarlayın. |
| Fiili bitişi ayarla                | Bu yaşam döngüsü durumuna güncelleştirildiğinde, kullanıcıdan iş emri için gerçek bitiş tarihi ve saati seçmesi istenirse bu seçeneği **Evet** olarak ayarlayın. |
| Günlükleri yazdır                 | Bir iş emri bu yaşam döngüsü durumuna güncelleştirildiğinde iş emri günlüklerinin otomatik olarak kaydedilmesi gerekiyorsa, bu seçeneği **Evet** olarak ayarlayın. Günlük deftere nakli sırasında hata oluşursa, bir ileti görüntülenir ve iş emri yaşam döngüsü durumunun güncelleştirilmesi iptal edilir. Bir iş emrine ait günlük satırlarını görüntülemek için **Kıymet yönetimi** \> **Ortak** \> **İş emirleri** \> **Tüm iş emirleri**, **Etkin iş emirleri**'ni seçin ya da **Etkin iş emirlerim** listeden seçin ve **Günlükler**'i seçin. Belirli bir yaşam döngüsü durumunda otomatik iş emri günlüğü deftere nakil işleminin bu kurulumu, **İş emri günlükleri** sayfasında **Günlükleri deftere naklet**'i seçmeniz ile aynıdır.<p>**Not:** Bu seçeneği **Evet** olarak ayarlarsanız, hiçbir onay iş akışı ayarlanmamışsa Günlükler otomatik olarak nakledilir. Şirketiniz **Günlük onay** sayfasında konfigüre edilen günlük onay kurulumunu kullanıyorsa (**Proje yönetimi ve muhasebe** \> **Kurulum** \> **Günlükler** \> **Günlük onayı**), bir yönetici veya memur tüketim kayıtlarını doğrulamanz ve deftere nakletmeniz gerekir.</p> |
| Bakım denetim listesini işle | Bir iş emri bu yaşam döngüsü durumuna güncellendiğinde tüm bağlı bakım kontrol listelerinin işlenmesi gerekiyorsa, bu seçeneği **Evet** olarak ayarlayın. Bu işlemenin bir parçası olarak, bir bakım denetim listesinde yapılan tüm sayaç kayıtları nakledilir ve tüm bakım denetim listesi sonucu değerlendirilir. **Başarılı** ve **Başarısız** bakım denetim listesi satırları değerlendirilir ve en az bir satır başarısız olursa tüm bakım denetim listesi kıymet yönetiminde **Başarısız** olarak işaretlenir. |
| Hazır                         | İş emri üzerinde oluşturulan tüm iş siparişi işleri için iş emri iş planlama çizelgeleme durumu **Evet** olarak ayarlandığında, iş emri bu yaşam döngüsü durumuna güncelleştirildiği sırada otomatik olarak **Hazır** durumuna güncelleştirilmelidir. |
| Başlangıç                         | İş emri üzerinde oluşturulan tüm iş siparişi işleri için iş emri iş planlama çizelgeleme durumu **Evet** olarak ayarlandığında, iş emri bu yaşam döngüsü durumuna güncelleştirildiği sırada otomatik olarak **Başlatıldı** durumuna güncelleştirilmelidir. |
| Son                           | İş emri üzerinde oluşturulan tüm iş siparişi işleri için iş emri iş planlama çizelgeleme durumu **Evet** olarak ayarlandığında, iş emri bu yaşam döngüsü durumuna güncelleştirildiği sırada otomatik olarak **Sona erdi** durumuna güncelleştirilmelidir. |
| Plan satırlarını sil         | Önceden sipariş edilmiş bir iş emrinde oluşturulan tüm iş emri işlerinde zamanlamanın, iş emri bu yaşam döngüsü durumuna güncellendiğinde silinmesi gerekiyorsa bu seçeneği **Evet** olarak ayarlayın. Başka bir deyişle, kıymetle ilgili kapasite rezervasyonları, ilişkili bakım görevlisi ve ilgili araçlar da silinir. Örneğin, bu seçeneği **Tahmini olarak** adlandırılan bir iş emri yaşam döngüsü durumunda **Evet** olarak ayarlarsınız. Yeniden çizelgeleme gerekli olduğundan, bir iş emri bu yaşam döngüsü durumuna geri alındığında, iş emri bu iş emrinde silinebilir. |

## <a name="set-up-project-stages-and-work-order-lifecycle-states"></a>Proje aşamalarını ve iş emri yaşam döngüsü durumlarını ayarla

1. **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri**'ni seçin.
2. **Proje aşaması** sekmesinde, kullanmak istediğiniz her aşama için, iş emirleriniz için gerekli olan her proje türüne ait onay kutusunu seçin. Proje türleri, izin verilen mali görevlerle ilgili kuralları tanımlar. Mali görevlere örnek olarak tahmin oluşturma, tahminler oluşturma ve başlangıç bakiyeleri gösterilebilir.

    > [!IMPORTANT]
    > Proje için proje aşaması seçilmezse, ancak proje aşaması bir iş emri yaşam döngüsü durumu için kullanılıyorsa, iş emri projeleri uygun şekilde güncelleştirilmez.

3. **Proje yönetimi ve muhasebe parametreleri** sayfasını kapatın.
4. **Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Yaşam döngüsü durumları**'nı seçin.
5. İş emri yaşam döngüsü durumu oluşturmak için **Yeni**'yi seçin.
6. **Yaşam döngüsü durumu** alanında yaşam döngüsü durumu kimliğini girin.
7. **Ad** alanına, bir ad girin.

    **Ayrıntılar** hızlı sekmesinde, **Yaşam döngüsü modelleri** alanı bu yaşam döngüsü durumunu kullanan iş emri yaşam döngüsü modellerinin sayısını gösterir.

8. **Genel** hızlı sekmesinde, **İş emri** bölümünde, ilgili seçenekleri **Evet** olarak ayarlayarak bu yaşam döngüsü durumu için kullanılabilir olması gereken işlevleri seçin. Seçeneklerin açıklamaları için, bu konunun önceki kısımlarında yer alan tabloya bakın.
9. **Proje** bölümünde, **Aşama** alanında, bu yaşam döngüsü durumuyla ilişkili olması gereken proje aşamasını seçin.
10. İş emri bu yaşam döngüsü durumunda olduğunda , her iş emri işiyle ilgili proje faaliyetleri otomatik olarak kapatılacağından, **Proje** bölümünde, **Tüm faaliyetleri kapat** seçeneğini **Evet** olarak ayarlayın.

    > [!NOTE]
    > Bir iş emri işiyle ilgili proje faaliyetinin numarasını bulmak için **Kıymet yönetimi** \> **Ortak** \> **İş emirleri** \> **Tüm iş emirleri**, **Etkin iş emirleri** ya da **Etkin iş emirlerim**'i seçin. İş emrini açın ve iş emri işini seçin. Faaliyet numarası **Satır ayrıntılar** hızlı sekmesinin **Genel** sekmesindeki **Proje** bölümünün **Etkinlik numarası** alanında gösterilir.

11. İş emri bu yaşam döngüsü durumundayken otomatik olarak iş emri günlüklerine yüklenmeliyse **Tahmini** bölümünde, **Çalışma saati tahminlerini kopyala**, **Öğeyi tahminini kopyala** ve / veya **Harcama tahminini kopyala** seçeneğini **Evet** olarak ayarlayın.
12. İş emri bu yaşam döngüsü durumunda olduğunda, iş emri işleriyle ilgili zamanlama durumu güncelleştirilecek ise, **Zamanlama** bölümünde seçeneklerden birini **Evet** olarak ayarlayın. **Hazır**, **Başlat**, **Bitir** ve **Planlanmış satırları sil** seçeneklerinin anlamları için bu konudaki önceki tabloya bakın.

    > [!NOTE]
    > Bir iş emri işiyle ilgili planlanmış satırları görmek için **Kıymet yönetimi** \> **Ortak** \> **İş emirleri** \> **Tüm iş emirleri**, **Etkin iş emirleri** ya da **Etkin iş emirlerim**'i seçin. İş emrini açın, **İş emri işleri** hızlı sekmesinde iş emri işini seçin ve **Satır ayrıntıları** hızlı sekmesinde görünümle ilgili bilgileri görüntüleyin. **Çizelge** sekmesindeki **Durum** alanı, iş emri işinin durumunu gösterir. **Durum** alanı şu değerlere ayarlanabilir: **Planlanan**, **Hazır**, **Başlatıldı**, **Durduruldu**, ve **Sona erdi**.

13. **Bakım istekleri** bölümünde, **Yaşam döngüsü durumu** alanında, ilgili bakım taleplerinin güncelleştirilmesi gereken bakım talebi yaşam döngüsü durumunu seçin. Bu güncelleştirme otomatik olarak gerçekleştirilir. Yalnızca bakım talebi için kullanılan bakım talebi yaşam döngüsü modelinde bakım talebi yaşam döngüsü durumu seçildiğinde yapılabilir.
14. İş emri güncelleştirildiğinde, bir iş emrinde kullanılan tüm maddelerin **Varlık ürün reçetesi** sayfasında otomatik olarak güncelleştirilmesi gerekiyorsa, **Varlık** bölümünde, **Varlık ürün reçetesini güncelleştir** seçeneğini **Evet** olarak ayarlayın. Bu ayar, örneğin, iş emri yaşam döngüsü durumu iş emrini tamamlandı veya bitmiş olarak tanımlarsa uygun olabilir.
15. **İş emri havuzu** bölümünde, bu yaşam döngüsü durumunda olan iş emirleri iş siparişi havuzlarından otomatik olarak silmek gerekliyse, **havuz başvurusunu sil** seçeneğini **Evet** olarak ayarlayın.
16. **Doğrula** hızlı sekmesinde, ilgili seçenekleri **Evet** olarak ayarlayarak bu yaşam döngüsü durumunda etkinleştirilmesi gereken doğrulama tiplerini seçin. Sonra, **Tür** alanında seçtiğiniz her doğrulama türü için, doğrulama türüyle ilişkili zorunlu alanlar doğrulanmadıysanız görüntülenecek olan ileti türünü seçin. **Hata** seçeneğini belirlerseniz, iş emri yaşam döngüsü durumu güncelleştirmesi, ilgili zorunlu alanlar iş emrinde güncelleştirilene kadar iptal edilir.

    - **Bakım kesinti süresi**, **Bakım denetim listesi**, **Hata belirtileri**, **Hata sebepleri**, ve **Hata giderme** seçenekleri **İş emri türleri** sayfasındaki **Zorunlu** bölümüne bağlıdır (**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **İş emri türleri**). Bu doğrulamaları etkinleştirmek için, ilgili seçeneklerin iş emri için kullanılan iş emri türünde de **Evet** olarak ayarlanması gerekir.
    - **Bakım denetim listesi** seçeneği bir iş emrinin güncelleştirildiği yaşam döngüsü durumu için **Evet** olarak ayarlanmışsa, doğrulama işlemi **Zorunlu** olarak işaretlenen bakım denetim listesi satırlarına **İşaretli** ya da **Uygun değil** olarak kaydettirilir. Bu kayıtlardan hiçbiri zorunlu satırlarda yapılmadıysa, iş emri bu yaşam döngüsü durumuna güncelleştirildiğinde bir bilgi, hata veya uyarı iletisi görüntülenir.
    - Bir çalışma emrinin güncelleştirildiği yaşam döngüsü durumu için **Taahhüt edilen maliyet** seçeneği **Evet** olarak ayarlanmışsa, toplam taahhüt edilen maliyet tutarı (yasal varlığın ödemeyi taahhüt edilen toplam gider tutarı) her iş emri için hesaplanır. Taahhüt edilen maliyet tutarı 0'dan (sıfır) fazla ise bir ileti gösterilir. Proje yönetimi ve hesap parametreleri sayfasındaki **Proje yönetimi ve muhasebe parametreleri** sayfasının **Maliyet kontrolü** sekmesindeki **Maliyet taahhütleri** hızlı sekmesindeki türleri seçin (**Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri**).
    - **Bakım kesinti süresi** seçeneği bir çalışma emrinin güncelleştirildiği yaşam döngüsü durumu için **Evet** olarak ayarlanmışsa, bakım kesinti süresi doğrulaması iş emriyle ilişkili olan kıymet üzerinde gerçekleştirilir. Bakım kesinti süresi kaydı yapılırsa ancak **Sona erdirilmiş** bir kayıt yoksa, iş emri bu yaşam döngüsü durumuna güncelleştirildiğinde bir ileti gösterilir.
    - Standart proje kurulumu, kıymet yönetimi kurulumunuz için gerekli tüm aşamaları içermiyorsa, **Proje yönetimi ve muhasebe parametreleri** sayfasının **Proje aşaması** sekmesinde Kullanıcı tanımlı proje aşamalarını ayarlayabilirsiniz. Aşağıdaki şekil **Proje yönetimi ve muhasebe parametreleri** sayfasındaki **Proje aşaması** sekmesini gösterir.

    ![Çeşitli proje türleri için proje aşamalarını ayarlama sayfası](media/10-setup-for-work-orders.png)

> [!NOTE]
> Bir iş emrini güncelleştediğiniz yaşam döngüsü durumu devre dışı ise, iş emriyle ilişkili, ancak henüz deftere nakledilmemiş Günlükler otomatik olarak silinir. Bu davranış, kullanılmayan verilerin otomatik olarak temizlenmesine yardımcı olur. (**Etkin** seçeneği **İş emri yaşam döngüsü** sayfasının **Genel** hızlı sekmesinde **Hayır** olarak ayarlanmışsa yaşam döngüsü durumu devre dışı bırakılır.)
>
> Bir iş emrini güncelleştediğiniz yaşam döngüsü durumını el ile devre dışı bıraktıysanız iş emriyle ilişkili, ancak henüz deftere nakledilmemiş Günlükler otomatik olarak **silinmez**. (Bir iş emrini el ile devre dışı bırakmak için **Kıymet yönetimi** \> **Ortak** \> **İş emirleri** \> **Tüm iş emirleri** ya da **Etkin iş emirleri**'ni seçin. İş emrini açın ve **Başlık** görünümüne geçin. **Genel** hızlı sekmesinde, **Düzenle**'yi seçin ve sonra **Etkin** seçeneğini **Hayır** olarak ayarlayın.)

## <a name="relations-among-work-order-lifecycle-models-work-order-types-and-work-order-lifecycle-states"></a>İş emri yaşam döngüsü modelleri, iş emri türleri ve iş emri yaşam döngüsü durumları arasındaki ilişkiler

Yaşam döngüsü modelleri iş akışlarına ve yaşam döngüsü durumları sırayla bir yaşam döngüsü modelinde seçilmiştir. Yaşam döngüsü modelleri, iş emri türlerinde ayarlanır. İş emri türleri, iş akışlarının ve çalışma işlemlerinin boyutunu veya kapsamını belirler. Örneğin, standart bir iş emri türü olan **Bakım**, birçok yaşam döngüsü durumuna sahip bir iş emri yaşam döngüsü modeliyle ilişkili olabilir. Bunun aksine, bir acil durum nedeniyle iş emri yapılmadan önce, planlanan iş siparişleri için veya işin tamamlandığı iş emirleri için kullanılan bir **Düzeltme** iş emri türüne sahip olabilirsiniz. Bu iş emri türü, yalnızca birkaç yaşam döngüsü durumu bulunan bir iş emri yalam döngüsü modeliyle ilişkili olabilir.

Türleri kullanma nedeni, örneğin bir iş emri veya bir kıymet üzerinde bir tür tanımlandığında, ilgili iş süreçleri (yaşam döngüsü durumları) otomatik olarak tanımlanır. İş emri türlerini ayarlamayla ilgili daha fazla bilgi için bkz. [İş emri türleri](../setup-for-work-orders/work-order-types.md).

> [!NOTE]
> İş emirlerinin yanı sıra, yaşam döngüsü durumları, yaşam döngüsü modelleri ve türleri işlem yapılacak yerleşimlere, varlıklara ve bakım taleplerine uygulanır.

Aşağıdaki şekil iş emri türleri, yaşam döngüsü modelleri ve yaşam döngüsü durumları arasındaki ilişkiyi gösterir.

![İş emri türü sayfası ile İş emri yaşam döngüsü modelleri sayfası karşılaştırması](media/11-setup-for-work-orders.png)

## <a name="work-order-lifecycle-models"></a>İş emri yaşam döngüsü modelleri

İş emri gerekli yaşam döngüsü durumları oluşturulduktan sonra, iş emirlerine veya yaşam döngüsü modellerine ayrılabilir. En azından, bir standart yaşam döngüsü modeli oluşturmalısınız.

1. **Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Yaşam döngüsü modelleri**'ni seçin.
2. İş emri yaşam döngüsü modeli oluşturmak için **Yeni**'yi seçin.
3. **Yaşam döngüsü modeli** alanında yaşam döngüsü modeli kimliğini girin.
4. **Ad** alanına, bir ad girin.

    **Ayrıntılar** hızlı sekmesinde, **Yaşam döngüsü durumları** alanı ilgili yaşam döngüsü modelinde seçili yaşam döngüsü durumlarının sayısını gösterir. **İş emri türleri** alanı bu yaşam döngüsü modelini kullanan iş emri türlerinin sayısını gösterir.

5. **Yaşam döngüsü durumları** hızlı sekmesinde yaşam döngüsü modeline eklenmesi gereken yaşam döngüsü durumlarını seçin:

    - Yaşam döngüsü modelinde bir yaşam döngüsü durumu kullanmak için durumu **Kalan yaşam döngüsü durumları** bölümünden seçin ve sağ ok düğmesini ![Sağ ok](media/12-setup-for-work-orders.png) seçerek durumu **Seçili yaşam döngüsü durumları** bölümüne taşıyın.
    - Yaşam döngüsü modelinde tüm kullanılabilir yaşam döngüsü durumlarını kullanmak için **Tüm kullanılabilir aşamaları seç** düğmesini ![Tüm kullanılabilir aşamaları seç](media/13-setup-for-work-orders.png) seçin. Tüm yaşam döngüsü durumları **Seçili yaşam döngüsü durumları** bölümüne aktarılır.
    - Yaşam döngüsü modelinden bir yaşam döngüsü durumunu kaldırmak için durumu **Seçili yaşam döngüsü durumları** bölümünden seçin ve sol ok düğmesini ![Sol ok](media/14-setup-for-work-orders.png) seçerek durumu **Kalan yaşam döngüsü durumları** bölümüne taşıyın.

6. Seçili yaşam döngüsü durumunu takip edebilecek yaşam döngüsü durumlarını tanımlamak için **Yaşam döngüsü durumu güncelleştirmeleri**'ni seçin.
7. **Güncelleştirmeler** hızlı sekmesinde, **Planlanan durum** alanında, iş emri zamanlamasını tamamladığınız bir iş emri için, önceki yaşam döngüsü durumuna bakmaksızın her zaman seçilmesi gereken iş emri yaşam döngüsü durumunu seçin.
8. **Zamanlanmamış yaşam döngüsü durumu** alanında, iş emri zamanlaması silinirse iş emri için her zaman seçilmesi gereken yaşam döngüsü durumunu seçin.
9. İş emri yaşam döngüsü modelini kaydedin.

![İş emri yaşam döngüsü modelleri sayfası](media/15-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]