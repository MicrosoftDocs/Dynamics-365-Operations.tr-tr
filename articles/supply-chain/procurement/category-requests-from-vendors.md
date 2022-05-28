---
title: Satıcılardan gelen kategori istekleri
description: Bu konuda, satıcıların kendi hesapları için tedarik kategorilerini nasıl isteyebileceği açıklanmaktadır. Ayrıca, tedarik aracıları tarafından tamamlanan onay işlemi de açıklanır.
author: GalynaFedorova
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9874151a5d82cc3441741489065877b78bab7bf5
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671224"
---
# <a name="category-requests-from-vendors"></a>Satıcılardan gelen kategori istekleri

[!include [banner](../includes/banner.md)]

Kategori talep süreci, satıcıların yeni tedarik kategorilerinin hesaplarıyla ilişkilendirilmesini talep etmelerine olanak tanır. Böylece, söz konusu tedarik kategorileri, ilgili tedarik ve kaynak işlemleri tarafından kullanılabilir. (Daha fazla bilgi için bkz. [Tedarik kataloglarına genel bakış](procurement-catalogs.md).)

Kategori istekleri, **Satıcı bilgileri** çalışma alanında satıcılar tarafından başlatılır. Ardından bunlar gözden geçirme ve onay için aracınıza gönderilir. Onaylanan kategoriler, satıcı hesabının tedarik kategorileri listesine eklenir.

## <a name="turn-the-category-requests-from-vendors-feature-on-or-off"></a>Satıcılardan gelen kategori istekleri özelliğini açma veya kapatma

Supply Chain Management sürüm 10.0.25 itibariyle, bu özellik varsayılan olarak açıktır. Yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Satıcıların, satıcı işbirliği üzerinden tedarik kategorilerine başvurmasına izin ver* özelliğini bularak bu işlevi açabilir veya kapatabilir.

Özellik etkinleştirilirse satıcı hesaplarına tedarik kategorilerini el ile eklemeye devam edebilirsiniz. Daha fazla bilgi için bkz. [Belirli tedarik kategorileri için satıcıları onaylama](tasks/approve-vendors-specific-procurement-categories.md).

## <a name="vendor-collaboration-requirements"></a>Satıcı işbirliği gereksinimleri

Bir satıcının kategori istekleriyle etkileşime geçebilmesi için satıcı işbirliği için gerekli ayarları yapmış olması gerekir.

Satıcının en az bir satıcı işbirliği kullanıcısı olmalıdır. Yalnızca *Satıcı yönetici (harici)* güvenlik rolüne sahip satıcı kullanıcıları kategori istekleri oluşturabilir ve gönderebilir.

Daha fazla bilgi için bkz. [Satıcı işbirliğini ayarlama ve sürdürme](set-up-maintain-vendor-collaboration.md).

## <a name="set-up-the-vendor-category-request-workflow"></a>Satıcı kategori talebi iş akışının kurulumu

*Satıcı kategori talebi* iş akışı, tedarik ve kaynak iş akışlarında ayarlanmalıdır. Satıcılar, inceleyip onaylayabileceğiniz yeni kategori istekleri gönderir. Kategori talebi onaylandıktan sonra talep edilen tedarik kategorileri satıcı hesabına eklenir.

Aşağıdaki örnek, tek bir onaylayanı olan basit bir *Satıcı kategori talebi* iş akışının nasıl ayarlanacağını gösterir. Aracınıza uygun iş akışı kurulumunu belirlemek için dahili işlemlerinizi gözden geçirmeniz gerekir.

1. **Tedarik ve kaynak atama \> Kurulum \> Tedarik ve kaynak atama iş akışları**'na gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. İletişim kutusunda, iş akışı düzenleyicisini açmak için **Satıcı kategori talebi iş akışı**'nı seçin.
1. İş akışı düzenleyicisinde oturum açın.
1. Eylem Bölmesi'nde, **Özellikler**'i seçin.
1. İş akışının **Özellikler** sayfasında, **Gönderim talimatları** alanında, talimat metnini girin. Talimatlar, bir kategori talebi gönderdiğinde satıcılar tarafından görülebilir.
1. **Özellikler** sayfasını kapatın.
1. **Yeni kategori talebini onayla** iş akışı öğesini tuvale sürükleyin.
1. **Başlat** iş akışı öğesinden **Yeni kategori talebini onayla** iş akışı öğesine bir bağlantı çekin.
1. **Yeni kategori talebini onayla** iş akışı öğesinden **Sonlandır** iş akışı öğesine bir bağlantı çekin.
1. **Yeni kategori talebini onayla iş akışı** öğesine çift dokunun (veya çift tıklayın).
1. **1. Adım** iş akışı öğesini seçin ve basılı tutun (veya sağ tıklatın) ve ardından **Özellikler**'i seçin.
1. İş akışı öğesinin **Özellikler** sayfasında, **İş öğesi konusu** alanında, konu metnini girin. Bu metin, **Bana atanan iş öğeleri** sayfasındaki **Konu** alanının değeri olarak gösterilir.
1. **İş öğesi yönergeleri** alanında, talimat metnini girin. Talimatlar, bir kategori talebinin Eylem Bölmesi'nde **İş akışı**'nı seçtiklerinde onaylayanlara görünür olur.
1. Sol bölmede **Atama**'yı seçin.
1. **Atama türü** sekmesinde, **Kullanıcıları bu iş akışı öğesine ata** seçeneğini *Kullanıcı* olarak belirleyin.
1. **Kullanıcı** sekmesinde, **Mevcut kullanıcılar** listesinden bir onaylayan seçin. Örneğin, Tedarik departmanında bir kullanıcı seçin.
1. Onaylayanı, **Seçili alanlar** listesine taşımak için sağ ok düğmesini (**\>**) seçin.
1. **Özellikler** sayfasını kapatın.
1. **Kaydet ve kapat**'ı seçin.
1. **Sürüm notları** alanında, iş akışıyla ilgili notları girin.
1. İş akışını kaydetmek için **Tamam**'ı seçin.
1. İş akışını test etmeye başlamaya hazırsanız **Yeni sürümü etkinleştir**'i seçin. Hazır değilseniz **Yeni sürümü etkinleştirme**'yi seçin.
1. İş akışı kurulumunu tamamlamak için **Tamam**'ı seçin.

> [!TIP]
> Aracınız, kategori taleplerinin onaylanmasını gerektirmiyorsa, iş akışını otomatik onay için yapılandırmalısınız.

İş akışı kurulumuyla ilgili daha fazla bilgi için bkz. [İş akışı sistemine genel bakış](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

## <a name="create-and-submit-a-category-request"></a>Kategori talebi oluşturma ve gönderme

Bu bölümde, satıcıların kategori talepleri oluşturmak, düzenlemek, görüntülemek ve göndermek için **Satıcı bilgileri** çalışma alanını nasıl kullanabileceği açıklanmaktadır.

### <a name="start-a-new-request"></a>Yeni talep başlatma

Yeni bir kategori talebi başlatmak için aşağıdaki adımları izleyin.

1. **Satıcı bilgileri** çalışma alanında, **Kategori talepleri** kutucuğunu seçin.
1. **Kategori talepleri** sayfasında, Eylem Bölmesinde, **Yeni kategori talebi**'ni seçin.
1. **Yeni kategori talebi** iletişim kutusunda, ağaca gidip/veya listenin en üstündeki filtreyi kullanarak, uygulamak istediğiniz kategoriyi bulun. İlgili her kategori için onay kutusunu seçin.

    Aaşağıdaki noktaları unutmayın:

    - Şu anda satıcı hesabınızda etkin olan kategoriler, seçili olarak gösterilir ve kaldırılamaz.
    - Tek bir kategori talebinde birden fazla tedarik kategorisi isteyebilirsiniz.

1. Taslak talebi oluşturmak için **Tamam**'ı seçin.

    Yeni taslak talebi artık **Kategori istekleri** sayfasında görünür.

1. Gerektiği şekilde gözden geçirmek ve düzenlemek için yeni taslak talebini açın.

    - Şu anda talebe dahil edilen kategorilerin listesini görüntülemek için, **Talep edilen kategoriler** hızlı sekmesini seçin.
    - Etkin kategorilerinizi görüntülemek için sayfanın sağ yanındaki **Etkin kategoriler** bilgi kutusunu açın.
    - Talebe bir kategori eklemek için, **Talep edilen kategoriler** hızlı sekmesindeki araç çubuğundan **Ekle**'yi seçin.
    - Talepten bir kategoriyi kaldırmak için **Talep edilen kategoriler** hızlı sekmesinde kategoriyi seçin ve araç çubuğundan **Kaldır**'ı seçin.
    - Talebe bir belge iliştirmek için Eylem Bölmesi'ndeki **Ekler**'i seçin. İliştirilen belgeler, kategori talebini gözden geçiren onaylayanlar tarafından görüntülenebilir.
    - Talebe iliştirilmiş bir belgeyi kaldırmak için Eylem Bölmesi'ndeki **Ekler**'i seçin. Kaldırılacak belgeyi seçin ve sonra Eylem bölmesinde **Sil**'i seçin.

1. İsteği göndermeye hazır olduğunuzda Eylem Bölmesi'nde **Gönder**'i seçin. Hazır değilseniz yalnızca sayfayı kapatın ve bu prosedürün kalan adımlarını atlayın. Daha sonra talebe tekrar geri dönebilirsiniz.
1. Görünen tüm gönderme talimatlarını okuyun ve **Gönder**'i seçin.
1. **Yorum** kutusuna gerekli ek bilgileri girin. Ardından talebi tamamlamak için **Gönder**'i seçin.

### <a name="edit-a-draft-or-recalled-request"></a>Bir taslağı veya geri çekilmiş talebi düzenleme

Bir taslağı veya geri çekilmiş talebi düzenlemek için aşağıdaki adımları izleyin.

1. **Satıcı bilgileri** çalışma alanında, **Kategori talepleri** kutucuğunu seçin.
1. Açmak için taslağı veya geri çekilen talebi seçin.
1. Talebi gerektiği şekilde düzenleyin ve ardından talebi kapatın ya da önceki prosedürde anlatıldığı şekilde gönderin.

### <a name="submit-a-draft-or-recalled-request"></a>Bir taslağı veya geri çekilmiş talebi gönderme

Bir taslağı veya geri çekilmiş talebi göndermek için aşağıdaki adımları izleyin.

1. **Satıcı bilgileri** çalışma alanında, **Kategori talepleri** kutucuğunu seçin.
1. Göndermek istediğiniz taslak veya geri çekilmiş talebi seçin.
1. Eylem Bölmesi'nde **Gönder**'i seçin.
1. Görünen tüm gönderme talimatlarını okuyun ve **Gönder**'i seçin.
1. **Yorum** kutusuna gerekli ek bilgileri girin. Ardından talebi tamamlamak için **Gönder**'i seçin.

    Kategori talebinin durumu, aşağıdaki değerlerden biri olarak değişir:

    - _Gözden geçirme bekleniyor_ – Talep iş akışında.
    - _Onay bekleniyor_ – Onay gereklidir.

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a>Henüz onaylanmamış gönderilen bir talebi geri çağırma

Gönderilen ancak henüz onaylanmamış bir kategori talebini geri çağırmak için aşağıdaki adımları izleyin.

1. **Satıcı bilgileri** çalışma alanında, **Kategori talepleri** kutucuğunu seçin.
1. Geri çekmek istediğiniz bekleyen talebi seçin.
1. Eylem Bölmesi'nde, **Geri çağır**'ı seçin.
1. **Bir yorum girin** kutusuna gerekli ek bilgileri girin. Ardından talebi tamamlamak için **Gönder**'i seçin.

    Kategori talebinin durumu _İptal edildi_ olarak değişir. Talebi silene veya yeniden başlatana kadar talep bu durumda kalır.

### <a name="delete-a-draft-or-recalled-request"></a>Bir taslağı veya geri çekilmiş talebi silme

Bir taslağı veya geri çekilmiş talebi silmek için aşağıdaki adımları izleyin.

1. **Satıcı bilgileri** çalışma alanında, **Kategori talepleri** kutucuğunu seçin.
1. Silmek istediğiniz taslak veya geri çekilmiş talebi seçin.
1. Eylem Bölmesi'nde **Sil**'i seçin.
1. Silmeyi onaylamak için **Evet**'i seçin.

### <a name="view-completed-requests"></a>Tamamlanan talepleri görüntüleme

Tamamlanan talepleri görüntülemek için **Satıcı bilgileri** çalışma alanını açın ve **Kategori talepleri** kutucuğunu seçin. Tamamlanmış kategori talepleri, aşağıdaki durumlardan birine sahip olacaktır:

- _Onaylandı_ – Talep onaylanmıştır. Yeni eklenen kategorileri görüntülemek için, **Satıcı bilgileri** çalışma alanına geri dönün, sol bölmedeki **Daha fazla ayrıntı** listesini açın ve **Kategoriler**'i seçin.
- _Reddedildi_ – Talep reddedilmiştir. Gerektiği şekilde yeni bir kategori talebi oluşturabilirsiniz.

## <a name="review-category-requests"></a>Kategori taleplerini gözden geçirme

Bu bölümde, satıcıların gönderdiği kategori taleplerinin nasıl denetleneceği, reddedileceği ve atanacağının yanı sıra tamamlanan taleplerin nasıl görüntüleneceği açıklanmaktadır. Bu iş akışı eylemleri, tüm kategori talebine yöneliktir.

### <a name="view-category-requests"></a>Kategori taleplerini görüntüleme

Kategori taleplerini görüntülemek için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak \> Satıcılar \> Satıcı işbirliği talepleri \> Kategori talepleri**'ne gidin.

    **Kategori talepleri** sayfası görüntülenir. Varsayılan sayfa görünümü, *Eylem bekleniyor* durumuna sahip kategori taleplerini gösterir.

1. Tüm talepleri görüntülemek için **Talepleri göster** alanından *Tümü*'nü seçin.
1. Gerektiği şekilde gözden geçirmek ve düzenlemek için talebi açın.

    - Şu anda talebe dahil edilen kategorilerin listesini görüntülemek için, **Talep edilen kategoriler** hızlı sekmesini seçin.
    - Etkin kategorileri görüntülemek için sayfanın sağ yanındaki **Etkin kategoriler** bilgi kutusunu açın.
    - Gönderilen belgeler varsa Eylem Bölmesindeki **Ekler** (ataş) düğmesi, iliştirilmiş belgelerin sayısını gösterir. İliştirilen belgeleri görmek için **Ekler** düğmesini seçin. Ardından görüntülenecek belgeyi seçin ve görüntülemek için **Aç**'ı seçin.
    - Talebe bir belge iliştirmek için Eylem Bölmesi'ndeki **Ekler**'i seçin. İliştirilen belgeler, kategori talebini gözden geçiren onaylayanlar tarafından görüntülenebilir.
    - Talebe iliştirilmiş bir belgeyi kaldırmak için Eylem Bölmesi'ndeki **Ekler**'i seçin. Kaldırılacak belgeyi seçin ve sonra Eylem bölmesinde **Sil**'i seçin.
    - İş akışı geçmişini görüntülemek için Eylem Bölmesi'nde **İş akışı**'nı seçin. İş akışı seçeneklerinde, **Diğer** ve ardından **İş akışı geçmişi**'ni seçin. **İş akışı geçmişi** sayfası görüntülenir.

### <a name="approve-a-pending-category-request"></a>Bekleyen kategori talebini onaylama

Bekleyen bir kategori talebini onaylamak için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak \> Satıcılar \> Satıcı işbirliği talepleri \> Kategori talepleri**'ne gidin.
1. Onaylanacak bekleyen talebi seçin.
1. Kategori talebini gözden geçirin.
1. İsteğe bağlı: **Genel** hızlı sekmesindeki **Neden kodu** alanında bir neden kodu seçin. Ardından **Neden açıklaması** alanına neden koduyla ilgili bir açıklama girin.
1. Eylem Bölmesinde **İş akışı**'nı seçin.
1. İş akışı seçeneklerinde **Onayla**'yı seçin.
1. **Yorum** alanına gerekli ek bilgileri girin. Ardından talebi tamamlamak için **Onayla**'yı seçin.

    Kategori talebinin durumu _Onaylandı_ olarak değiştirilir ve tedarik kategorileri satıcı hesabına eklenir.

### <a name="reject-a-pending-category-request"></a>Bekleyen kategori talebini reddetme

Bekleyen bir kategori talebini reddetmek için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak \> Satıcılar \> Satıcı işbirliği talepleri \> Kategori talepleri**'ne gidin.
1. Reddedilecek bekleyen talebi seçin.
1. Kategori talebini gözden geçirin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Genel** hızlı sekmesindeki **Neden kodu** alanında bir neden kodu seçin. Ardından **Neden açıklaması** alanına neden koduyla ilgili bir açıklama girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem Bölmesinde **İş akışı**'nı seçin.
1. İş akışı seçeneklerinde, **Diğer** ve ardından **Reddet**'i seçin.
1. **Yorum** alanına gerekli ek bilgileri girin. Ardından talebi tamamlamak için **Reddet**'i seçin.

    Kategori talebinin durumu _Reddedildi_ olarak değişir. Bu aşamada, satıcı gerektiği şekilde yeni bir kategori talebi oluşturabilir.

### <a name="delegate-a-pending-category-request"></a>Bekleyen kategori talebini atama

Bekleyen bir kategori talebini başka bir kullanıcıya atamak için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak \> Satıcılar \> Satıcı işbirliği talepleri \> Kategori talepleri**'ne gidin.
1. Onaylamak istediğiniz bekleyen talebi seçin.
1. Eylem Bölmesinde **İş akışı**'nı seçin.
1. İş akışı seçeneklerinde, **Diğer** ve ardından **Ata**'yı seçin.
1. **Kullanıcı** alanında, kategori talebinin gözden geçirilmek üzere atanacağı kullanıcıyı seçin.
1. **Yorum** alanına gerekli ek bilgileri girin.
1. Atama işlemini tamamlamak için **Ata**'yı seçin. Seçili kullanıcı artık kategori talebini gözden geçirebilir.

### <a name="view-procurement-categories-for-a-vendor"></a>Bir satıcıya ait tedarik kategorilerini görüntüleme

Kategori talebi onaylandıktan sonra talep edilen tedarik kategorilerini görüntülemek için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak \> Satıcılar \> Tüm satıcılar**'a gidin.
1. **Tüm satıcılar** sayfasında, tedarik kategorilerini görüntülemek istediğiniz satıcıyı seçin.
1. Eylem Bölmesi'nde, **Genel** sekmesini açın ve **Ayarla** grubundan **Kategoriler**'i seçin.

    **Kategoriler** sayfası görüntülenir. **Tedarik** hızlı sekmesi, kategori talebiyle eklenen tedarik kategorilerini gösterir.

1. **Tedarik** hızlı sekmesinde gerektiği şekilde değişiklik yapabilirsiniz. Örneğin, **Satıcı kategorisi durumu** alanını _Tercih edilen_ olarak ayarlayabilirsiniz.
