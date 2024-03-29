---
title: "\"Yeterli kapasite bulunamadı\" planlama altyapısı hatasını ve sınırlı kapasiteyi düzeltme"
description: Bu makalede, "%1 üretim emri planlanamadı" hatasının nedenleri ve çözümleri hakkında bilgi sağlanmaktadır. Yeterli kapasite bulunamadı" planlama altyapısı hatasını gidermenize yardımcı olacak bir bağlantı sağlanmaktadır..
author: t-benebo
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4f54c06a07b3cdd0b8fe2cc52614189ff31ba7f
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135614"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>"Yeterli kapasite bulunamadı" planlama altyapısı hatasını düzeltme

[!include [banner](../includes/banner.md)]

Planlamayı çalıştırdığınızda aşağıdaki hata iletisini alabilirsiniz:

> %1 üretim emri zamanlanamadı. Yeterli kapasite bulunamadı.

Planlama altyapısının başarısız olmasının ve bu hata iletisinin alınmasının birkaç nedeni vardır. Bu makalede, hatanın temel nedenini bulmanıza ve ardından bu nedeni hafifletmenize yardımcı olacak yönergeler sağlanmaktadır.

## <a name="review-the-applicable-resources"></a>Uygun kaynakları inceleme

Bu hata, üretim emri sitesinde işlem gereksinimlerini karşılayan uygun kaynak bulunmadığında oluşabilir.

Uygun kaynakları incelemek için şu adımları izleyin.

1. **Üretim denetimi \> Üretim emirleri \> Tüm üretim emirleri** bölümüne gidin ve planlanamayan üretim emrini açın veya seçin.
1. Eylem Bölmesinde, **Üretim emri** sekmesinde **Üretim ayrıntıları** grubunda **Rota**'yı seçin.
1. **Üretim rotası** sayfasında, operasyonu seçin ve ardından Eylem Bölmesi'nde **Uygun kaynaklar**'ı seçin.
1. **Uygun kaynaklar** iletişim kutusunda, **Gereksinimleri şunun için kullan** alanını kullandığınız planlama türüne bağlı olarak *İşlemleri planlama* veya *İş planlama* olarak ayarlayın.
1. Üretim emri sitesinde uygun kaynakların bulunduğundan emin olun.

## <a name="review-the-calendars-that-are-associated-with-resources"></a>Kaynaklarla ilişkilendirilen takvimleri inceleme

Kaynak veya kaynak grubuyla ilişkilendirilen bir takvim yoksa ya da ilişkili takvim doğru ayarlanmadıysa (örneğin, çalışma zamanı yoksa veya yüzde olarak verimliliği 0 \[sıfır\] ise) bu hata oluşabilir.

Takvimin kaynak veya kaynak grubuyla ilişkilendirildiğini doğrulamak için şu adımları izleyin.

1. **Üretim denetimi \> Üretim emirleri \> Tüm üretim emirleri** bölümüne gidin ve planlanamayan üretim emrini açın veya seçin.
1. Eylem Bölmesinde, **Üretim emri** sekmesinde **Üretim ayrıntıları** grubunda **Rota**'yı seçin.
1. **Üretim rotası** sayfasında, operasyonu seçin ve ardından Eylem Bölmesi'nde **Uygun kaynaklar**'ı seçin.
1. **Uygulama kaynakları** iletişim kutusunda, kaynağı seçin ve ardından **Kaynağı görüntüle**'yi seçin. Alternatif olarak, **Kaynak grubu** alanını seçin ve basılı tutun (veya sağ tıklayın) ve ardından **Ayrıntıları görüntüle**'yi seçin.
1. **Kaynaklar** sayfasında veya **Kaynak grupları** sayfasında, **Takvimler** hızlı sekmesinde, bir takvimin kaynak ya da kaynak grubuyla ilişkilendirildiğinden emin olun.

> [!NOTE]
> İşlem planlama çizelgeleme sırasında hata oluşursa bir takvimin tüm uygun kaynak gruplarıyla ilişkilendirildiğinden emin olmanız gerekir.

Takvim kurulumunu incelemek için şu adımları izleyin.

1. **Kuruluş yönetimi \> Kurulum \> Takvimler \> Takvimler** bölümüne gidin ve kaynak veya kaynak grubuyla ilişkilendirilen takvimi seçin.
1. Eylem Bölmesinde **Çalışma zamanları**'nı seçin.
1. **Çalışma zamanları** sayfasında, sayfanın boş olmadığından emin olun. Ayrıca ilgilendiğiniz günler için **Denetim** alanının *Kapalı* olarak ayarlanmadığından, çalışma zamanlarının mevcut olduğundan ve **Verimlilik yüzdesi** alanının *0* (sıfır) olarak ayarlanmadığından emin olun.

Takvim, temel takvimle ilişkilendirilmişse temel takvimin kurulumunu da incelemeniz gerekir.

> [!NOTE]
> İşlem planlama çizelgelemede, kaynak grubunun takvimi her işlemin başlangıç ve bitiş saatlerini ve tarihlerini belirlemek için kullanılır. Ayrıca sistemin belirli bir kaynak grubundaki belirli bir gün için belirli bir işlemi planlayabileceği süreyi de sınırlar. Örneğin, belirli bir gündeki bir kaynak grubunun çalışma zamanı 08:00 - 16:00 arasındaysa bir işlemin kaynak grubuna yüklediği yük, kaynak grubunun ilgili gündeki kullanılabilir kapasite miktarından bağımsız olarak sekiz saate sığabilecek yükü aşamaz. Ancak kullanılabilir kapasite, yükü daha fazla sınırlayabilir.

## <a name="review-the-scheduling-parameters"></a>Planlama parametrelerini inceleme

İyi bir performans sağlamak için planlama altyapısı yalnızca belirli bir süre ve belirli sayıda planlama çakışması için bir kaynağı arar.

Planlama parametrelerini incelemek için şu adımları izleyin.

1. **Kuruluş yönetimi \> Kurulum \> Planlama parametreleri** bölümüne gidin.
1. Şu adımlardan birini izleyin:

    - **Planlama zaman aşımı etkin** seçeneği *Hayır* olarak ayarlanmışsa 3. adıma geçin.
    - **Planlama zaman aşımı etkin** seçeneği *Evet* olarak ayarlanmışsa işlemenin tamamlanma süresini uzatmak için **Sıra başına maksimum planlama zamanı** alanının değerini artırın.

1. Şu adımlardan birini izleyin:

    - **Planlamayı en iyi duruma getirme zaman aşımı etkin** seçeneği *Hayır* olarak ayarlanmışsa 4. adıma geçin.
    - **Planlamayı en iyi duruma getirme zaman aşımı etkin** seçeneği *Evet* olarak ayarlanmışsa işlemenin tamamlanma süresini uzatmak için **En iyi duruma getirme denemeleri zaman aşımı** alanının değerini artırın.

1. Sayfadaki ayarları değiştirdiyseniz tekrar denemek için emri yeniden planlayın.

## <a name="review-capacity"></a>Kapasiteyi inceleme

Sınırlı planlama gerçekleştirdiğinizde ancak boş kapasite olmadığında bu hata oluşabilir.

Sonsuz kapasite planlaması gerçekleştirmek için şu adımları izleyin.

1. **Üretim denetimi \> Üretim emirleri \> Tüm üretim emirleri** bölümüne gidin ve planlanamayan üretim emrini seçin veya açın.
1. Eylem Bölmesi'nde, **Planla** sekmesinde, **Üretim emri** grubunda **İşlemleri planla** veya **İşleri planla**'yı seçin.
1. **İşlemleri planlama** veya **İşleri planlama** iletişim kutusunda, **Sınırlı kapasite** seçeneğini *Hayır* olarak ayarlayın.
1. Emri planlamak için **Tamam**'ı seçin.

Kaynaktaki kullanılabilir kapasiteyi incelemek için şu adımları izleyin.

1. **Kuruluş yönetimi \> Kaynaklar \> Kaynaklar** bölümüne gidin ve planlanamayan emre uygun bir kaynağı seçin.
1. Eylem Bölmesi'nde, **Kaynak** sekmesinde, **Görüntüle** grubunda, **Kapasite yükü** veya **Kapasite yükü, grafik olarak** seçeneğini belirleyin ve kullanılabilir kapasite olduğundan emin olun.

Kaynak grubundaki kullanılabilir kapasiteyi incelemek için şu adımları izleyin.

1. **Kuruluş yönetimi \> Kaynaklar \> Kaynak grupları** bölümüne gidin ve planlanamayan emre uygun bir kaynak grubu seçin.
1. Eylem Bölmesi'nde, **Kaynak grup** sekmesinde, **Görüntüle** grubunda,**Kapasite yükü** veya **Kapasite yükü, grafik olarak** seçeneğini belirleyin ve kullanılabilir kapasite olduğundan emin olun.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Ana planlama, kaynak takvim kapatıldığında bir kaynağı ayırır

Operasyon planlama kullanırken master planlama, birincil kaynak grubunun takvimine göre kapasite planlayacaktır. İkincil operasyonu birincil işlemle aynı zamanda kitap içine alıp, ikincil operasyonun takvimlerini veya kapasitesini dikkate almaz. Bu, üretim emrinin kapalı bir takvimde veya ikincil operasyonun kullanılabilir olmadığı bir zamanda zamanlanmasına (takvim kapalı, kapasite yok) neden olabilir.

İş planlama kullanırken, master planlama sipariş planlarken hem birincil hem de ikincil operasyonun kapasitesini ve takvimini dikkate alır. Siparişin planlanması için her iki operasyonun kaynakları için takvimler açık olması ve kullanılabilir kapasiteye sahip olması gerekir.

## <a name="maximum-job-lead-time-is-too-short"></a>Maksimum iş bekleme süresi çok kısa

Planlama altyapısı, siteniz için belirlenen **Maksimum iş teslim süresi** varsayılan sipariş ayarlarında veya kapsam ayarlarında bir öğe için belirtilen müşteri adayı süresinden daha kısa ise bir sipariş planlayamaz.

Siteniz için **Maksimum iş müşteri adayı süresi** ayarını görüntülemek veya düzenlemek için **Üretim denetimi \> Kurulum \> Üretim denetimi parametreleri** bölümüne gidin **Genel** sekmesini açın.

Bir öğeyle ilgili olarak varsayılan sipariş ayarlarını görüntülemek veya düzenlemek için aşağıdaki adımları izleyin:

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Listede, ilgili ürünü bulun ve seçin.
1. Eylem Bölmesinde, **Stok yönetimi** sekmesini açın ve **Varsayılan sipariş ayarları** nı seçin.
1. **Stok** hızlı sekmesini genişletin ve **Stok müşteri adayı süresi** ayarını gerektiği şekilde düzenleyin.

Bir öğeyle ilgili olarak kapsam ayarlarını görüntülemek veya düzenlemek için aşağıdaki adımları izleyin:

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Listede, ilgili ürünü bulun ve seçin.
1. Eylem Bölmesi'nde **Plan** sekmesini açın ve **Öğe kapsamı** nı seçin.
1. **Müşteri adayı süresi** sekmesini açın **Üretim süresi** değerini gerektiği gibi görüntüleyin veya düzenleyin.

## <a name="excessive-quantity-of-required-resources"></a>Gerekli kaynakların aşırı miktarda olması

Planlama sırasında altyapı, bir rota işlemi için gerekli kaynak miktarı setini operasyon kaynak gereksinimlerine göre uygulanabilir kaynaklarla eşleştirmeye çalışır. Kaynak miktarını çok yüksek ayarlanması bir rotanın gerçekleştirilemez olmasına yol açabilir ve bu da planlama hatasına neden olur.

Seçili bir ürün, rota ve rota işlemiyle ilgili belirtilen miktarı ve uygulanabilir kaynakları denetlemek için aşağıdaki yordamı kullanın:

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Kılavuzda, ilgili ürünü bulun ve seçin.
1. Eylem Bölmesinde, **Mühendis** sekmesini açın ve **Rota**'yı seçin.
1. Kılavuzda, ilgili rotayı bulun ve seçin.
1. Sayfanın altındaki **Genel bakış** sekmesine açın.
1. Seçilen rota işlemleri listesinden bir işlem seçin.
1. Seçili rota operasyonuyla ilgili uygulanabilir kaynakları görüntüleyebileceğiniz bir iletişim kutusu açmak için **Uygulanabilir kaynakları** seçin.
1. **Kaynak yükü** sekmesini açın. Buradaki **Miktar** alanı, seçilen rota işlemi için gerekli kaynak miktarını gösterir. Gerektiği gibi görüntüleyin ve/veya düzenleyin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
