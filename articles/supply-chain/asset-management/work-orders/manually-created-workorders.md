---
title: El ile oluşturulmuş iş emirleri
description: Bu konuda Varlık Yönetimi'nde el ile iş emirleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875944"
---
# <a name="manually-created-work-orders"></a>El ile oluşturulmuş iş emirleri

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


İş emirlerini el ile iki şekilde oluşturabilirsiniz.

- **Tüm iş emirlerinde** veya **Etkin iş emirlerinde**  
- **Tüm bakım istekleri** veya **Etkin bakım istekleri** veya **İşlem yapılacak yerleşim bakım isteklerim**'de  

## <a name="create-work-order"></a>İş emri oluştur

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. **Yeni** düğmesine tıklayın.

3. **İş emri oluştur** açılır listesinde, bir iş emri türü seçin.

4. Gerekirse, bir açıklama seçin.

5. İş emri için varlığı ve bir bakım işi türü seçin.

>[!NOTE]
>Bir varlık seçtiğinizde, kullanılabilir üç sekme bulunur: **Varlıklarım** sekmesi, tahsis edilebileceğiniz (sistemde oturum açan bakım çalışanı) işlem yapılacak yerleşimlerle ilgili varlıkları içerir (şurada ayarlanır: [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md)). [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md) formundaki bir bakım görevlisi için işlem yapılacak yerleşimler ayarlanmadıysa, **Varlıklarım** sekmesi görünür olmaz. **Etkin varlıklar** sekmesi, varlık yaşam döngüsü durumu "Etkin" olan tüm varlıkların listesini içerir. **Varlık görünümü** sekmesi, işlem yapılacak yerleşimlerin ve bu yerleşimlerde kurulu olan varlıkların ağaç görünümünü gösterir.

6. Gerekirse, **Bakım işi türü çeşidi** ve **İşlem**'i seçin.

7. Gerekirse, **Servis düzeyi** alanında iş emri hizmet düzeyini değiştirebilirsiniz.

8. İlgili alanlarda beklenen başlangıç ve bitiş tarihlerini seçin.

9. Yeni iş emri oluşturmak için **Tamam**'a tıklayın.

10. Gerekirse, iş emrini **Tüm iş emirleri**'nde düzenleyin.

- **Tüm iş emirleri**'nde, **İş emri bakım işleri** hızlı sekmesinde satırlar ekleyerek, Ayrıntılar görünümünde iş emrine birden fazla varlık ekleyebilirsiniz. Bir varlıkta, yalnızca varlık için seçilen varlık türünde tanımlanan bakım işi türlerini seçebilirsiniz.  
- Bir iş emrinde kullandıktan sonra bir varlık servis düzeyi veya varlık kritikliğini değiştirdiyseniz (bkz. [Varlık servis düzeyleri](../setup-for-objects/object-priorities.md) ve [Varlık kritiklikleri](../setup-for-objects/object-criticalities.md)), iş emrindeki servis düzeyi veya kritiklik uygun şekilde güncelleştirilmez.
- İş emrindeki kritiklik, iş emrine bir iş emri satırı eklendiğinde veya silindiğinde yeniden hesaplanır.
- **Tüm iş emirleri** Ayrıntılar görünümü > **Başlık** görünümü > **Zamanlama** hızlı sekmesinde, **Sorumlu grup** veya **Sorumlu** alanlarında bir sorumlu bakım görevlisi grubu veya sorumlu bakım görevlisi seçebilirsiniz. Bu ayarlar, örneğin iş emri yaşam döngüsü durumu değiştiğinde, iş emri etkin olduğu sürece değiştirilebilir. İş emri oluşturma sırasında otomatik seçim, **Sorumlu bakım görevlileri** kurulumuna dayanır. Bir iş emri oluşturduktan sonra iş emri işlerini ekler veya kaldırırsanız ve iş emrini güncelleştirdiğinizde **Sorumlu grup** ve **Sorumlu** alanı boşsa, Varlık Yönetimi kurulum formunda sorumlu bir çalışan grubu veya sorumlu bakım görevlisi için olası bir eşleşme arar. İş emrini güncelleştirdiğinizde **Sorumlu grup** veya **Sorumlu** alanı zaten doldurulmuş durumda ise, hiçbir değişiklik yapılmaz. 

- **Bakım durumu**'nda gelen ve tamamlanan iş emirleriyle ilgili iş yükünün özetini almak için hesaplama yapabilirsiniz.  

- **Satır ayrıntıları** hızlı sekmesinde, iş emri işinde seçilen varlığa coğrafi koordinatlar eklemek için **Enlem** ve **Boylam** alanlarını kullanın.  

## <a name="create-related-work-order"></a>İlgili iş emri oluştur

Örneğin, birincil ve ikincil iş emirleriyle çalışmak istiyorsanız, varolan bir iş emri için ilgili iş emrini oluşturabilirsiniz. Yeni bir iş emri, varolan bir iş emrinden alınan bir iş emri işine dayalıdır.

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. İlişkili bir iş emri oluşturmak istediğiniz iş emrini seçin.

3. **İlgili iş emri** öğesine tıklayın.

4. **İlgili iş emri oluştur** açılır iletişim kutusunda, **İş emri işi** alanında ilgili iş emrini oluşturmak istediğiniz iş emri işini seçin.

5. **Bakım işi türü** alanında bir bakım işi türü seçin ve gerekirse **Bakım işi türü çeşidi** ve **İşlem** alanlarında ilgili bir bakım işi türü çeşidi ve işlem seçin.

6. Bu yaptığınız ilk ilgili iş emriyse, **Yeni iş emri** radyo düğmesine tıklatın.

7. İlgili alanlarda **İş emri türü** ve **Açıklama** seçin.

8. Gerekirse, **Servis düzeyi** alanında iş emri hizmet düzeyini değiştirin.

9. İlgili alanlarda beklenen başlangıç ve bitiş tarihlerini ekleyin.

10. **Tamam**'a tıklayın. Yeni ilgili iş emri **Tüm iş emirleri** listesinde gösterilir.

11. Zaten ilişkili iş emirleri olan bir iş emrinde ilgili bir iş emri oluşturursanız, iş emri işini zaten ilgili bir iş emrine ekleyebilirsiniz. Bu işlem, adım 6'da **İlgili çalışma emrine ekle** düğmesine tıklayarak gerçekleştirilir. Daha sonra, yeni bir iş emri işi eklemek istediğiniz ilgili iş emrini seçersiniz. **Hizmet düzeyi**, **Beklenen başlangıç** ve **Beklenen** bitiş alanlarını gerektiği gibi düzenleyin ve **Tamam**'a tıklayın. İş emri işi varolan ilgili iş emrine eklenir.


![Şekil 1](media/03-work-orders.png)

**Not:** **Varlık yönetimi parametreleri** > **İş emirleri** bağlantısı > **İlgili iş emri maskesi** alanında ilgili iş emri maskesi ayarlarsanız, iş emri kodları maske ayarına uygun şekilde oluşturulur. İlgili bir iş emri maskesi ayarlanmamışsa, ilgili iş emirleri için sonraki kullanılabilir iş emri kodu kullanılır.

## <a name="copy-work-order"></a>İş emrini kopyala

Varolan bir iş emrinden hızlı şekilde yeni bir iş emri oluşturmak mümkündür. İş emirleriyle çalışmanın bu yolu, bakım planlarını temel alan iş emirleri oluşturmaktan farklıdır. Örneğin, farklı varlıklarda düzenli aralıklarla tamamlanması gereken çeşitli işler içeren birçok iş emri işi bulunan bir iş emriniz varsa yararlıdır.

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. İçeriğini kopyalamak istediğiniz iş emrini seçin.

3. **İş emrini kopyala** öğesine tıklayın. Seçilen iş emrinden alınan iş emri kurulumu görüntülenir. Gerekirse, alanların bazılarını düzenleyebilirsiniz.

4. Yeni iş emri oluşturmak için **Tamam**'a tıklayın.

5. Gerekirse, iş emrini **Tüm iş emirleri**'nde düzenleyin.

>[!NOTE]
>Yeni iş emri oluşturulduğunda, bazı bilgiler doğrudan varolan iş emrinden kopyalanır. Tahminler, araçlar, bakım denetim listeleri, işlem yapılacak yerleşim, adresler ve zamanlama ile ilgili bilgiler kopyalanmaz, ancak Varlık yönetiminde geçerli kurulumdan başlatılır. Bu, ilk iş emri oluşturma zamanından iş emrinin bir kopyasını aldığınız zamana kadar bu verilerde değişiklikler yapılmışsa, bu değişikliklerin oluşturduğunuz yeni iş siparişine dahil edildiği anlamına gelir. Örnekler tahminlerdeki değişiklikler veya güncelleştirilmiş bakım denetim listeleridir.


![Şekil 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a>Bakım talebine dayalı iş emri oluşturma

1. **Varlık yönetimi** > **Ortak** > **Bakım talepleri** > **Tüm bakım talepleri** ya da **Etkin bakım talepleri**'ni seçin.

2. İş emri oluşturmak istediğiniz bakım talebini seçin ve **Düzenle** öğesine tıklayın.

3. **Tüm talepler**'de **İş emri** seçeneğine tıklayın.

4. **İş emri** açılır menüsünü doldurun. Bakım talebinde bir bakım işi türü seçilmişse, iş emrini oluştururken gerekirse başka bir bakım işi türü seçebilirsiniz.

5. **Tamam**'a tıklayın. İş emrinin oluşturulduğunu bildiren bir ileti görüntülenir.

6. Bir bakım talebine hangi iş emirlerinin bağlı olduğunu görmek istiyorsanız, **Tüm bakım talepleri** veya **Etkin bakım talepleri** listelerinde bakım talebini seçin ve **İş emirleri** düğmesine tıklayın.


![Şekil 3](media/05-work-orders.png)


>[!NOTE]
>İş emirleri, bakım planı işlerini planlayarak veya bir varlıkta bakım planlarını veya bakım sıralarını "otomatik oluştur" özelliği ayarlanarak otomatik olarak oluşturulabilir. **Bakım zamanlamasında** bakım taleplerinden oluşturulan iş emirleri, bakım taleplerinde seçilen bakım işi türleriyle oluşturulur.

