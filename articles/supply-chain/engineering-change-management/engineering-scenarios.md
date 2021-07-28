---
title: Mühendislik değişikliği yönetimi özelliği kılavuzu
description: Bu konu, mühendislik değişikliği yönetimiyle nasıl çalışılacağını gösteren uçtan uca bir kılavuz sağlar.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 9440471d6983136971878c8ee9e327d4dd407833
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346166"
---
# <a name="engineering-change-management-feature-walkthrough"></a>Mühendislik değişikliği yönetimi özelliği kılavuzu

[!include [banner](../includes/banner.md)]

Bu konu, mühendislik değişikliği yönetimiyle nasıl çalışılacağını gösteren uçtan uca bir kılavuz sağlar. En önemli senaryoların her birini ele alır:

- Temel özellik yapılandırması
- Bir mühendislik şirketi yeni mühendislik ürünlerini nasıl oluşturur?
- Bir mühendislik şirketi mühendislik ürünlerini yerel bir şirkete nasıl serbest bırakır?
- Yerel bir şirket, bir mühendislik şirketi tarafından serbest bırakılan bir ürünü nasıl inceleyebilir ve kabul edebilir?
- Yerel bir şirket standart hareketlerde mühendislik ürünlerini nasıl kullanabilir?
- Bir mühendislik ürünü satış siparişine nasıl eklenir?
- Mühendislik değişikliği isteği oluşturarak mühendislik ürününde değişiklik isteğinde nasıl bulunulur?
- Mühendislik değişikliği emri oluşturarak istenen değişiklikler nasıl zamanlanır ve uygulanır?
- Değiştirilen bir ürün nasıl serbest bırakılır?

Bu konudaki tüm alıştırmalar Microsoft Dynamics 365 Supply Chain Management için sağlanan standart örnek verileri kullanır. Ayrıca, her alıştırma önceki alıştırmayı geliştirerek ilerler. Bu nedenle, özellikle mühendislik değişikliği yönetimi özelliğini daha önce hiç kullanmadıysanız, baştan sona alıştırmalar üzerinde çalışmanızı öneririz. Bu şekilde, özelliği tam olarak kavrayabilirsiniz.

## <a name="set-up-for-the-sample-scenario"></a>Örnek senaryo için ayarlar

Bu konuda sağlanan örnek senaryoyu izlemek için öncelikle demo verilerini kullanılabilir hale getirerek ve birkaç özel kayıt ekleyerek özelliği hazırlamanız gerekir.

Bu konunun geri kalanında herhangi bir alıştırma yapmaya başlamadan önce, aşağıdaki tüm alt bölümlerdeki talimatları izleyin. Bu alt bölümler, kendi kuruluşunuz için mühendislik değişikliği yönetimini ayarlarken kullanacağınız birkaç önemli ayar sayfasını da tanıtır.

### <a name="make-standard-demo-data-available"></a>Standart demo verilerini kullanılabilir hale getirme

[Standart demo verilerinin yüklü olduğu](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) bir sistem üzerinde çalışın. Standart demo verileri, çeşitli demo tüzel kişilikler (şirketler ve kuruluşlar) için veri ekler. Alıştırmalarda ilerlerken, bir *mühendislik kuruluşu* olarak ayarlanmış bir şirket *(DEMF)* ile *operasyonel kuruluş* olarak ayarlanmış başka bir şirket *(USMF)* arasında geçiş yapmak için gezinti çubuğunun sağ tarafındaki şirket seçici kullanacaksınız.

### <a name="set-up-an-engineering-organization"></a>Mühendislik kuruluşunu ayarlama

Mühendislik verilerinin sahibi bir mühendislik kuruluşu, ürün tasarımı ve ürün değişikliklerinden sorumludur. Mühendislik kuruluşunuzu ayarlamak için aşağıdaki adımları izleyin.

1. **Mühendislik değişikliği yönetimi &gt; Kurulum &gt; Mühendislik kuruluşları**'na gidin.
1. Kılavuza satır eklemek için **Ekle**'yi seçin ve aşağıdaki değerleri ayarlayın:

    - **Mühendislik kuruluşu:** *DEMF*
    - **Kuruluş adı:** *Contoso Entertainment System Germany*

    ![Mühendislik kuruluşu ekleme.](media/engineering-org.png "Mühendislik kuruluşu ekleme")

### <a name="set-up-the-version-product-dimension-group"></a>Sürüm ürün boyutu grubunu ayarlama

1. **Ürün bilgileri yönetimi &gt; Kurulum &gt; Boyutlar ve varyant grupları &gt; Ürün boyutu grupları**'na gidin.
1. Bir ürün boyutu grubu oluşturmak için **Yeni**'yi seçin.
1. **Ad** alanını *Sürüm* olarak ayarlayın.
1. Yeni boyutu kaydetmek ve değerleri **Ürün boyutları** hızlı sekmesine yüklemek için **Kaydet** seçin.
1. **Ürün boyutları** hızlı sekmesinde, etkin ürün boyutu olarak **Sürüm**'ü ayarlayın.

    ![Ürün boyut grubu ekleme.](media/product-dimension-groups.png "Ürünu boyut grubu ekleme")

### <a name="set-up-product-lifecycle-states"></a>Ürün yaşam döngüsü durumlarını ayarlama

Bir mühendislik ürünü yaşam döngüsü boyunca ilerlerken her yaşam döngüsü durumu için hangi hareketlere izin verileceğini belirlemeniz önemlidir. Ürün yaşam döngüsü durumlarını ayarlamak için aşağıdaki adımları izleyin.

1. **Mühendislik değişikliği yönetimi &gt; Kurulum &gt; Ürün yaşam döngüsü durumu**'na gidin.
1. Yaşam döngüsü durumu eklemek için **Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:

    - **Durum:** *Operasyonel*
    - **Açıklama:** *Operasyonel*

1. Yeni yaşam döngüsü durumunu kaydetmek ve değerleri **Etkin iş süreçleri** hızlı sekmesine yüklemek için **Kaydet** seçin.
1. **Etkin iş süreçleri** hızlı sekmesinde, kullanılabilir olması gereken iş süreçlerini seçin. Bu örnekte, tüm iş süreçleri için **İlke** alanını *Etkin* olarak bırakın.

    ![Yaşam döngüsü durumu için iş süreçlerini etkinleştirme.](media/product-lifecycle-states-1.png "Yaşam döngüsü durumu için iş süreçlerini etkinleştirme")

1. Başka bir yaşam döngüsü durumu eklemek için **Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:

    - **Durum:** *Prototip*
    - **Açıklama:** *Prototip*

1. Yeni yaşam döngüsü durumunu kaydetmek ve değerleri **Etkin iş süreçleri** hızlı sekmesine yüklemek için **Kaydet** seçin.
1. **Etkin iş süreçleri** hızlı sekmesinde, kullanılabilir olması gereken iş süreçlerini seçin. Bu örnekte, tüm iş süreçleri için **İlke** alanını *Uyarıyla etkin* olarak bırakın.

    ![Yaşam döngüsü durumu için iş süreçlerini etkinleştirme (uyarılarla).](media/product-lifecycle-states-2.png "Yaşam döngüsü durumu için iş süreçlerini etkinleştirme (uyarılarla)")

### <a name="set-up-a-version-number-rule"></a>Sürüm numarası kuralı ayarlama

1. **Mühendislik değişikliği yönetimi &gt; Kurulum &gt; Ürün sürüm numarası kuralı**'na gidin.
1. Kural eklemek için **Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:

    - **Ad:** *Otomatik*
    - **Sayı kuralı:** *Otomatik*
    - **Biçim:** *V-\#\#*

    ![Ürün sürüm numarası kuralı ekleme.](media/version-number-rule.png "Ürün sürüm numarası kuralı ekleme")

### <a name="set-up-a-product-release-policy"></a>Ürün serbest bırakma ilkesi ayarlama

1. **Mühendislik değişikliği yönetimi &gt; Kurulum &gt; Ürün serbest bırakma ilkeleri**'ne gidin.
1. Serbest bırakma ilkesi eklemek için **Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:

    - **Ad:** *Bileşenler*
    - **Açıklama:** *Bileşenler*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Ürün türü:** *Madde*
    - **Şablonları uygulayın:** *Her Zaman*
    - **Etkin:** *Evet*

1. **Tüm ürünler** hızlı sekmesinde, satır eklemek için **Ekle**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **Şirket:** *DEMF*
    - **Şablon serbest bırakılan ürün:** *D0006*

1. **Ekle**'yi seçerek bir satır daha ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Şirket hesapları kodu:** *USMF*
    - **Şablon serbest bırakılan ürün:** *D0006*
    - **Ürün reçetesi al:** Bu onay kutusunu seçin.
    - **Ürün reçetesi onayını kopyala:** Bu onay kutusunu seçin.
    - **Ürün reçetesi etkinleştirmesini kopyala:** Bu onay kutusunu seçin.
    - **Rotayı al:** Bu onay kutusunu seçin.
    - **Rota onayını kopyala:** Bu onay kutusunu seçin.
    - **Rota etkinleştirmesini kopyala:** Bu onay kutusunu seçin.

    ![Ürün serbest bırakma ilkesi ekleme.](media/product-release-policy.png "Ürün serbest bırakma ilkesi ekleme")

### <a name="set-up-an-engineering-product-category"></a>Mühendislik ürünü kategorisi ayarlama 

Mühendislik ürünü kategorileri mühendislik ürünleri (diğer bir şekilde, mühendislik değişikliği yönetimi yoluyla sürümü oluşturulmuş ve denetlenen ürünler) oluşturmak için temel oluşturur. Mühendislik ürünü kategorileri ayarlamak için aşağıdaki adımları takip edin.

1. **Mühendislik değişikliği yönetimi &gt; Mühendislik ürünü kategorisi ayrıntıları**'na gidin.
1. Bir kategori oluşturmak için **Yeni**'yi seçin.
1. **Ayrıntılar** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Ad:** *Bileşenler*
    - **Mühendislik kuruluşu:** *DEMF*
    - **Ürün türü:** *Madde*
    - **Hareketlerde sürümü izleme:** *Evet*
    - **Ürün boyutu grubu:** *Sürüm*
    - **Oluşturma aşamasında ürün yaşam döngüsü durumu:** *Operasyonel*
    - **Sürüm numarası kuralı:** *Otomatik*
    - **Geçerliliği zorla:** *Hayır*
    - **Numara kuralı terminolojisini kullan:** *Hayır*
    - **Ad kuralı terminolojisini kullan:** *Hayır*
    - **Açıklama kuralı terminolojisini kullan:** *Hayır*

1. **Serbest bırakma ilkesi** hızlı sekmesinde, **Ürün serbest bırakma ilkesi** alanını *Bileşenler* olarak ayarlayın.
1. **Kaydet**'i seçin.

    ![Mühendislik ürün kategorisi ayarlama.](media/product-category-details.png "Mühendislik ürün kategorisi ayarlama")

### <a name="set-up-product-acceptance-conditions"></a>Ürün kabul koşullarını ayarlama

1. *USMF* tüzel kişiliğine (şirket) geçmek için gezinti çubuğunun sağ tarafındaki şirket seçicisini kullanın.
1. **Mühendislik değişikliği yönetimi &gt; Kurulum &gt; Mühendislik değişikliği yönetimi parametreleri**'ne gidin.
1. **Serbest bırakma denetimi** sekmesinde, **Ürün kabulü** bölümünde, **Ürün kabulü** alanını *El ile* olarak ayarlayın.

    ![Ürün kabulü koşullarını ayarlama.](media/engineering-change-management-parameters.png "Ürün kabulü koşullarını ayarlama")

## <a name="create-a-new-engineering-product"></a>Yeni bir mühendislik ürünü oluşturma

Mühendislik ürünü, mühendislik değişikliği yönetimi yoluyla sürümü oluşturulmuş ve denetlenen bir üründür. Başka bir deyişle, değişiklikleri ömrü boyunca denetleyebilirsiniz ve değişiklik bilgileri mühendislik değişikliği emirleri kullanılarak kaydedilir. Mühendislik ürünleri oluşturmak için şu adımları izleyin.

1. Mühendislik kuruluşunuzun tüzel kişiliğinde olduğunuzdan emin olun (bu örnekte *DEMF*). Gerektiğinde gezinti çubuğu sağ tarafındaki şirket seçicisini kullanın.
1. Aşağıdaki adımlardan birini izleyerek **Serbest bırakılan ürünler** sayfasını açın.

    - **Ürün bilgi yönetimi &gt; Ürünler &gt; Serbest bırakılmış ürünler**'e gidin.
    - **Mühendislik değişikliği yönetimi &gt; Ortak &gt; Serbest bırakılan ürünler**'e gidin.

1. Eylem Bölmesi'nde, **Ürün** sekmesindeki **Yeni** gurubunda **Mühendislik**'nü seçin.
1. **Yeni ürün** iletişim kutusunda aşağıdaki değerleri ayarlayın.

    - **Mühendislik Ürünü Kategorisi:** *Bileşenler*
    - **Ürün numarası:** *Z0001*
    - **Ürün adı:** *Hoparlör seti*

    ![Mühendislik ürünü ekleme.](media/new-product-dialog.png "Mühendislik ürünü ekleme")

    **Sürüm** alanının, daha önce ayarladığınız ürün sürüm numarası kuralını kullanarak otomatik olarak ayarladığını unutmayın.

1. Ürün oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni ürünün ayrıntılar sayfası açılır. **Depolama boyut grubu**, **İzleme boyutu grubu** ve/veya **Madde modeli grubu** gibi bazı alanlar için değerlerin zaten doldurulduğuna dikkat edin. Ürün *DEMF* tüzel kişiliğine serbest bırakıldığı ve *Bileşenler* mühendislik ürün kategorisiyle ilişkili *Bileşenler* ürün serbest bırakma ilkesini kullandığından, bu alanlar otomatik olarak ayarlanır. Daha önce *DEMF* tüzel kişiliği için bir satır ayarlamak üzere şablon olarak *D0006* maddesini kullandığınız için doldurulan değerler *D0006* maddesinden alınmıştır.

    ![Serbest bırakılan ürün ayrıntıları.](media/product-details.png "Serbest bırakılan ürün ayrıntıları")

1. Eylem Bölmesi'nde, **Mühendis** sekmesinde, **Mühendislik değişikliği yönetimi** grubunda, **Mühendislik sürümleri**'ni seçerek ürünün sürümlerini görüntüleyin.

    ![Mühendislik sürümleri.](media/engineering-versions-list.png "Mühendislik sürümleri")

1. **Mühendislik sürümleri** sayfasında, ürün için yalnızca bir sürüm olduğunu ve etkin olduğunu unutmayın.
1. Ayrıntılarını görüntülemek için sürümü seçin.

    ![Mühendislik sürümü ayrıntıları.](media/engineering-version-details.png "Mühendislik sürümü ayrıntıları")

1. **Mühendislik sürümü** sayfasında, **Ürün reçetesi** hızlı sekmesinde **Ürün reçetesi oluştur**'u seçin.
1. **Ürün reçetesi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Ürün reçetesi numarası:** Z0001
    - **Ad:** Hoparlör seti
    - **Tesis:** 1

    ![BOM oluşturma.](media/create-bom.png "BOM oluşturma")

1. Ürün reçetesi eklemek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.
1. **Ürün reçetesi** hızlı sekmesinde **Ürün reçetesi**'ni seçin.
1. **Ürün reçetesi** sayfasında, **Ürün reçetesi satırları** hızlı sekmesinde, üç satır ekleyin; *D0001*, *D0003* ve *D0006* maddeleri için birer tane olmalıdır.

    ![Ürün reçetesi satırları ekleme.](media/bom.png "Ürün reçetesi satırları ekleme")

1. **Kaydet**'i seçin.
1. Sayfayı kapatın.
1. **Mühendislik sürümü** sayfasında, **Ürün reçetesi** hızlı sekmesinde **Onayla**'yı seçin.
1. Görünen iletişim kutusunda **Tamam**'ı seçin.

    ![Ürün reçetesini onaylama.](media/approve-dialog.png "Ürün reçetesini onaylama")

1. **Mühendislik sürümü** sayfasında, **Ürün reçetesi** hızlı sekmesinde **Etkinleştir**'i seçin.
1. **Etkin** ve **Onaylandı** onay kutularının ürün reçetesi için seçili olduğuna dikkat edin.

    ![Etkin ve onaylanan ürün reçetesi.](media/approved-bom.png "Etkin ve onaylanan ürün reçetesi")

1. Sayfayı kapatın.

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a>Mühendislik ürünlerini yerel bir şirkete serbest bırakma

Ürün artık Mühendislik departmanı tarafından tasarlanmıştır. Bu örnekte, ürün, mühendislik departmanının bir müşteri için tasarladığı bir prototiptir. Müşteri, *USMF* tüzel kişiliğinin müşterisi olduğundan, ürünün bu tüzel kişiliğe serbest bırakılması gerekir.

1. Tüzel kişiliği *DEMF* olarak ayarlayın. (Gerektiğinde gezinti çubuğu sağ tarafındaki şirket seçicisini kullanın.)
1. **Ürün bilgi yönetimi &gt; Ürünler &gt; Serbest bırakılmış ürünler**'e gidin.
1. *Z0001* ürününü seçin.
1. Eylem bölmesinde, **Ürün** sekmesinde, **Bakım** grubunda, **Ürün yapısını serbest bırak**'ı seçerek **Ürünleri serbest bırak** sihirbazını açın.
1. **Serbest bırakılacak mühendislik ürünlerini seç** sayfasında, *Z0001* ürünü için **Seç** onay kutusunu işaretleyin.

    ![Serbest bırakılacak mühendislik ürünlerini seçme.](media/select-eng-product-to-release.png "Serbest bırakılacak mühendislik ürünlerini seçme")

1. **Serbest bırakma ayrıntıları**'nı seçin.
1. Serbest bırakılacak ürünün ayrıntılarını ve ürün yapısını inceleyebileceğiniz **Ürün serbest bırakma ayrıntıları** sayfası görüntülenir. **Ürün reçetesi gönder** seçeneğinin *Evet* olarak ayarlanmış olduğuna dikkat edin. Bu nedenle, hem *Z0001* ürünü ve ürün reçetesindeki tüm alt öğeleri serbest bırakılacaktır.

    Ayrıntıları gözden geçirmek için sol bölmedeki herhangi bir alt öğeyi seçebilirsiniz. Herhangi bir alt öğenin ürün reçetesi varsa o alt öğenin ürün reçetesini serbest bırakmayı da seçebilirsiniz.

    ![Ürün serbest bırakma ayrıntılarını gözden geçirme.](media/product-release-details.png "Ürün serbest bırakma ayrıntılarını gözden geçirme")

1. **Ürünleri serbest bırak** sihirbazına dönmek için sayfayı kapatın.
1. **Serbest bırakılacak ürünleri seçin** sayfasını açmak için **İleri**'yi seçin. Herhangi bir standart (mühendislik dışı) ürün seçmiş olsaydınız, bunlar bu sayfada görünürdü. **Ürün yapısını serbest bırak**'ı seçerek standart bir ürün serbest bıraktığınızda, ürünün ürün reçetesi ve rotasının da serbest bırakılacağını unutmayın.

    ![Serbest bırakılacak standart ürünleri seçme.](media/select-std-product-to-release.png "Serbest bırakılacak standart ürünlerini seçme")

1. **Serbest bırakılacak ürün varyantlarını seçin** sayfasını açmak için **İleri**'yi seçin. Bu örnekte, herhangi bir varyant yoktur.
1. **Şirketleri seçin** sayfasını açmak için **ileri**'yi seçin.
1. Ürünün serbest bırakılacağı şirketleri seçin. Bu örnekte, **USMF** için onay kutusunu seçin.

    ![Serbest bırakılacak şirketleri seçme.](media/select-release-companies.png "Serbest bırakılacak şirketleri seçme")

1. **Seçimi onaylayın** sayfasını açmak için **ileri**'yi seçin.
1. **Bitir**'i seçin.

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a>Ürünü yerel şirkette serbest bırakmadan önce gözden geçirin ve kabul edin

Mühendislik departmanı artık ürünün kullanılacağı yerel şirketlere bilgi yayınlamıştır. Bu örnekte, yerel şirket *USMF*'dir.

**Ürün kabulü** alanını *USMF* şirketi için **Mühendislik değişikliği yönetimi parametreleri** sayfasında *El ile* olarak ayarladığınızdan, ürünlerin o şirkete serbest bırakılmadan önce el ile kabul edilmesi gerekir. Başka bir deyişle, serbest bırakılmadan önce gözden geçirilmeli ve kabul edilmelidir.

Ürünü gözden geçirmek ve *USMF* şirketine serbest bırakmak için aşağıdaki adımları izleyin.

1. Tüzel kişiliği *USMF* olarak ayarlayın. (Gezinti çubuğunun sağ tarafındaki şirket seçicisini kullanın.)
1. **Mühendislik değişikliği yönetimi &gt; Ortak &gt; Ürün serbest bırakmaları &gt; Açık ürün serbest bırakmaları**'na gidin.

    **Açık ürün serbest bırakmaları** sayfası, *Kabul edilmeyi bekliyor* durumundaki *Z0001* ürününü gösterir.

    ![Ürün serbest bırakma işlemlerini açma.](media/open-product-releases.png "Ürün serbest bırakma işlemlerini aç")

1. **Ürün serbest bırakma ayrıntıları** sayfasını açmak için **Ürün numarası** sütunundaki değeri seçin. Aşağıdaki ayrıntılara dikkat edin:

    - **Genel** hızlı sekmesi, serbest bırakan şirket (bu örnekte *DEMF*), serbest bırakma tesisi (*1*) ve alan tesis (*1*) gibi ürün serbest bırakma hakkındaki bilgileri gösterir. **Ürünleri serbest bırak** sihirbazında alıcı bir tesis belirtmediğiniz için serbest bırakılan tesis değeri alıcı tesise kopyalanır.
    - **Serbest bırakma ayrıntıları** hızlı sekmesi, ürün ve serbest bırakılan sürümü hakkında bilgi gösterir. Burada, geçerlilik tarihi gibi ayarları değiştirebilirsiniz.
    - **Rota** hızlı sekmesi, ürünün rotasını gösterir. Ancak, bu örnekte, herhangi bir rota serbest bırakmadınız.

    ![Ürün serbest bırakma ayrıntıları.](media/product-release-details-2.png "Ürün serbest bırakma ayrıntıları")

1. Bilgileri gözden geçirmeyi tamamladığınızda, ürünü kabul etmeye ve bu şekilde *USMF* şirketine serbest bırakmaya hazır olursunuz. Eylem Bölmesinde, **Eylemler &gt; Kabul Et**'i seçin.
1. Ürün artık *USMF* şirketine serbest bırakılır. **Ürün bilgi yönetimi &gt; Ürünler &gt; Serbest bırakılmış ürünler**'e gidin. *Z0001* maddesini görürsünüz.

## <a name="use-the-product-in-transactions-in-the-local-company"></a>Ürünü yerel şirketteki hareketlerde kullanma

*USMF* şirketinin ana veri yöneticisi, kullanıcıların yanlışlıkla üzerinde çalıştıkları işlemlere eklemeleri halinde uyarılmalarını sağlamak için ürünün *Prototip* durumunda olduğundan emin olmak istiyor.

1. **Ürün bilgi yönetimi &gt; Ürünler &gt; Serbest bırakılmış ürünler**'e gidin.
1. *Z0001* ürününü seçerek ürünün ayrıntılar sayfasını açın. (Ürünü bulmak için filtreyi kullanabilirsiniz.)
1. Eylem Bölmesi'nde, **Mühendis** sekmesinde, **Mühendislik değişikliği yönetimi** grubunda, **Mühendislik sürümleri**'ni seçin.
1. **Mühendislik sürümleri** sayfasında, ayrıntılar sayfasını açmak için *V-01* sürümünü seçin.
1. Eylem Bölmesi'nde, **Ürün** sekmesindeki **Yaşam döngüsü durumu** gurubunda **Yaşam döngüsü durumunu değiştir**'i seçin.
1. **Yaşam döngüsü durumunu değiştir** açılır iletişim kutusunda, **Durum** alanını *Prototip* olarak ayarlayın ve ardından **Tamam**'ı seçin.

    ![Yaşam döngüsü durumunu değiştirme.](media/change-lifecycle-state.png "Yaşam döngüsü durumunu değiştirme")

## <a name="add-the-engineering-product-to-a-sales-order"></a>Bir mühendislik ürününü satış siparişine ekleme

Ürün artık müşteriye satılabilir. Ürünü bir satış siparişine eklemek için bu adımları izleyin.

1. **Satış ve pazarlama &gt; Satış siparişleri &gt; Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, **Müşteri hesabı** alanını *US-0002* olarak ayarlayın ve **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesinde, bir satır ekleyin ve bunun için **Madde numarası** alanını *Z000* olarak ayarlayın.
1. Eylem bölmesinde, **Kaydet**'i seçin.

    Maddenin *Prototip* durumunda olduğunu bildiren bir uyarı iletisi alırsınız. Ancak, ileti sadece bir uyarı olduğundan, satış siparişi yine de oluşturulmuştur.

    ![Bir mühendislik ürünü için satış siparişi.](media/sales-order-eng-product.png "Bir mühendislik ürünü için satış siparişi")

## <a name="request-changes-in-the-engineering-product"></a>Mühendislik ürününde değişiklik isteği

Ürün bir müşteriye gönderildi ancak müşteri tam olarak memnun kalmadı ve iyileştirme önerileri içeren geri bildirim sağladı. Müşteri telefonda bir satış görevlisi ile konuşurken, satış görevlisi müşterinin tanımladığı değişiklikleri isteyebilir.

1. **Satış ve pazarlama &gt; Satış siparişleri &gt; Tüm satış siparişleri**'ne gidin.
1. Önceki alıştırmada oluşturduğunuz satış siparişini bulup açın.
1. **Satış siparişi satırları** hızlı sekmesinde, **Mühendislik değişikliği yönetimi &gt; Yeni mühendislik değişikliği isteği**'ni seçin.

    ![Satış siparişinden mühendislik değişikliği isteği oluşturma.](media/sales-order-eng-change-request.png "Satış siparişinden mühendislik değişikliği isteği oluşturma")

1. Müşterinin geri bildirimine göre mühendislik değişikliği isteğini doldurun. Bu örnekte, aşağıdaki değerleri ayarlayın:

    - **Değişiklik isteği:** *555*
    - **Başlık:** *Z0001 müşteri değişikliği*
    - **Öncelik:** *düşük*
    - **Kategori:** ayar değişikliği
    - **Önem derecesi:** *Orta*

1. **Bilgi** hızlı sekmesinde, kılavuza not eklemek için **Yeni &gt; Not**'u seçin.
1. Yeni notun **Açıklama** alanında, *D0003* maddesinin ürün reçetesinden silinmesi gerektiğini belirtin. Nota daha fazla bilgi eklemeniz gerekiyorsa **Notlar** alanına metin girebilirsiniz.

    ![Mühendislik değişiklik isteği.](media/eng-change-request.png "Mühendislik değişiklik isteği")

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Maddenin **Ürünler** hızlı sekmesine otomatik olarak eklendiğine ve mühendislik değişikliği isteğinin kaynağının (satış siparişi) **Kaynak** hızlı sekmesine eklendiğine dikkat edin.

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a>Mühendislik değişikliği emrini kullanarak üründe değişiklik yapma

Satış görevlisi ürünün önemli olduğunu ve özellikle müşteri için tasarlandığını bilmektedir. Bu nedenle, satış görevlisi *DEMF* şirketindeki bir mühendisi arayıp değişiklik isteği hakkında bilgi verir. Bu şekilde, mühendis süreci hızlandırabilir.

Mühendis şimdi müşteriden gelen isteği gözden geçirir ve ürün için bir değişiklik emri oluşturur.

1. Mühendis *DEMF* şirketinde çalıştığı için tüzel kişiliği *DEMF* olarak ayarlayın. (Gezinti çubuğunun sağ tarafındaki şirket seçicisini kullanın.)
1. **Mühendislik değişikliği yönetimi &gt; Ortak &gt; Mühendislik değişikliği istekleri**'ne gidin.
1. Değişiklik isteği *555*'i açın.
1. Bilgileri gözden geçirin ve değişikliği onaylayın. Eylem Bölmesi'nde, **Değişiklik isteği** sekmesindeki **Durumu değiştir** grubunda **Onayla**'yı seçin.
1. **Mühendislik değişikliği yönetimi &gt; Ortak &gt; Mühendislik değişikliği emirleri**'ne gidin.
1. Eylem Bölmesinde, bir değişiklik emri oluşturmak için **Yeni**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **Değişiklik emri:** *555*
    - **Başlık:** *Z0001 müşteri değişikliği*
    - **Kategori:** *Müşteri değişikliği*
    - **Öncelik:** *Düşük*
    - **Önem derecesi:** *Orta*

1. **Etkilenen ürünler** hızlı sekmesinde, kılavuza satır eklemek için **Yeni &gt; Ekle**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **Ürün:** *Z0001*
    - **Etki:** *Yeni sürüm*

    ![Mühendislik değişiklik emri oluşturma.](media/eng-change-order.png "Mühendislik değişikliği emri oluşturma")

1. **Etki** alanını *Yeni sürüm* olarak ayarladığınızda, **Ürün ayrıntıları** hızlı sekmesinin **Ayrıntılar** sekmesindeki **Yeni sürüm** alanı yeni sürüm numarasının ne olacağını gösterir (bu örnekte *V-02*).

    ![Mühendislik değişikliği emri için ürün ayrıntıları.](media/eng-change-order-product-details.png "Mühendislik değişikliği emri için ürün ayrıntıları")

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Ürün ayrıntıları** hızlı sekmesinde, *Z0001* ürününün *V-01* sürümünün ürün reçetesini açmak için **Ürün reçetesi** sekmesinde **Satırlar**'ı seçin.

    ![Mühendislik ürünü ürün reçetesi satırları.](media/eng-product-bom-lines.png "Mühendislik ürünü ürün reçetesi satırları")

1. *D0003* madde numarası için satırı seçin ve ardından Eylem Bölmesinde **Sil**'i seçin. Bu satırın **Değişiklik türü** alanının değeri *Silindi* olarak değişir.
1. Eylem bölmesinde, **Kaydet**'i seçin.

    ![Değiştirilen mühendislik ürünü ürün reçetesi satırları.](media/eng-product-bom-lines-modified.png "Değiştirilen mühendislik ürünü ürün reçetesi satıraları")

1. **Mühendislik değişikliği emri** sayfasına dönmek için **Ürün reçetesi satırı** sayfasını kapatın.
1. **Ürün ayrıntıları** hızlı sekmesinde, **Ürün reçetesi** sekmesinde, *Z0001* ürün reçetesi için **Değişiklik türü** alanının değerinin artık *Değiştirildi* olduğuna dikkat edin.

    ![Değiştirilmiş bir ürün reçetesi içeren mühendislik değişikliği emri.](media/eng-change-order-changed-bom.png "Değiştirilmiş bir ürün reçetesi içeren mühendislik değişikliği emri")

    Değişikliklerin işlenebilmesi için emrin onaylanması gerekir. Değişiklikler işlendiğinde, ürünler mühendislik değişikliği emrine dahil edilen değişikliklerle güncelleştirilir. Bu örnekte, mühendislik değişikliği emrini oluşturan kişi onaylayıcı olarak belirtilmiştir.

1. Eylem Bölmesi'nde, **Değişiklik emri** sekmesindeki **Durumu değiştir** grubunda **Onayla**'yı seçin.
1. Ürünün bilgilerini güncelleştirmek için **İşle**'yi seçin.

## <a name="release-the-changed-product"></a>Değiştirilen ürünü serbest bırakma

Ürün artık *USMF* şirketine yeniden serbest bırakılabilir ve daha sonra müşteriye gönderilebilir. Ürünü doğrudan mühendislik değişiklik emrinden serbest bırakmak için aşağıdaki adımları izleyin.

1. Önceki alıştırmada oluşturduğunuz mühendislik değişikliği emrini zaten açık değilse açın.
1. Eylem Bölmesi'nde, **Değişiklik emri** sekmesindeki **Ürün serbest bırakmaları** grubunda **Ara**'yı seçin.
1. Arama sonuçları, etkilenen ürünlerin hangi şirketlere serbest bırakıldığını gösterir. Arama sonuçlarını kapatın.
1. Eylem Bölmesi'nde, **Değişiklik emri** sekmesinde, **Ürün serbest bırakmaları** grubunda, önceki aramanın sonuçlarını görebileceğiniz **Serbest bırakmalar** iletişim kutusunu açmak için **Görüntüle**'yi seçin.
1. Ürünleri serbest bırakmak istediğiniz her şirketi seçin.
1. **Serbest bırakmalar** iletişim kutusunu kapatıp değişiklik emrine dönmek için **Tamam**'ı seçin.
1. Eylem Bölmesi'nde, **Değişiklik emri** sekmesinde, **Ürün serbest bırakmaları** grubunda, etkilenen ürünleri seçilen şirketlere serbest bırakmak için **İşle**'yi seçin. Alternatif olarak, serbest bırakma işlemini başlatmak için **Ürün yapısını serbest bırak**'ı seçin.

## <a name="complete-the-change-order"></a>Değişiklik sırasını tamamlama

Başka eylem kalmadığını göstermek üzere değişiklik sırasını tamamlandı olarak işaretlemek için Eylem Bölmesi'nde **Tamamla**'yı seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
