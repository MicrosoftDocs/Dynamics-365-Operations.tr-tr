---
title: Vergi Hesaplamayı kullanmaya başlama
description: Bu konuda, Vergi Hesaplamasının nasıl ayarlanacağı açıklanmaktadır.
author: wangchen
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3f8aa791cee1926afe6be347331d47902a3b7304
ms.sourcegitcommit: f4dc09601bceb5cdc88ee184ce7c8f369e3e6e86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2021
ms.locfileid: "6060575"
---
# <a name="get-started-with-the-tax-calculation-preview"></a>Vergi Hesaplama (Önizleme) kullanmaya başlama

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Bu konu, Vergi Hesaplama'yı kullanmaya başlama hakkında bilgi sağlar. Öncelikle, Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) ve Dynamics 365 Finance ile Dynamics 365 Supply Chain Management içindeki yapılandırma adımlarını izlemeniz konusunda yol gösterir. Daha sonra, Finance ve Supply Chain Management işlemlerinde Vergi Hesaplama özelliklerinin kullanımıyla ilgili genel işlemi inceler.

Ayarlama dört ana adımdan oluşur:

1. LCS'de Vergi Hesaplama eklentisini yükleyin.
2. RCS'de, Vergi Hesaplama özelliğini ayarlayın. Bu ayar bir tüzel kişiliğe özgü değildir. Finance ve Supply Chain Management tüzel kişileri arasında paylaşılabilir.
3. Finance ve Supply Chain Management'ta tüzel kişiliğe göre Vergi Hesaplama parametrelerini ayarlayın.
4. Finance ve Supply Chain Management'ta satış siparişleri gibi işlemler oluşturun ve vergileri belirlemek ve hesaplamak için Vergi Hesaplama eklentisini kullanın.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki prosedürleri tamamlamadan önce, aşağıdaki önkoşulların yerine getirilmesi gerekir:

- LCS hesabınıza erişiminiz var ve bir LCS projesini Dynamics 365 sürüm 10.0.18 veya sonrasını çalıştıran bir katman 2 (veya daha sonrası) ortamıyla [KB4616360](https://fix.lcs.dynamics.com/Issue/Details?kb=4616360&bugId=568738&dbType=3&qc=1f1c04ff39adad74ef871f539e8d73e14c1893ef7cc4b6e3f7d5c5864ec2781a) veya sonraki sürümüyle dağıttınız.
- RCS hesabınıza erişiminiz var.
- Dağıtılmış Finance veya Supply Chain Management ortamınızda denemeyi etkinleştirmek için Microsoft ile bağlantı kurdunuz.

## <a name="set-up-tax-calculation-in-lcs"></a>LCS'de Vergi Hesaplama'yı ayarlama

1. [LCS'te](https://lcs.dynamics.com) oturum açın
2. Microsoft Power Platform tümleştirmesi için kurulumu tamamlayın. Daha fazla bilgi için bkz. [Eklentiler sekmesi](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Dağıtılmış üretim dışı ortamlarınızdan birini seçin ve sonra **Yeni bir eklenti yükle**'yi seçin.
4. **Vergi Hesaplama (önizleme)** öğesini seçin.
5. Hüküm ve koşulları okuyup kabul edin ve sonra **Yükle**'yi seçin.

## <a name="set-up-tax-calculation-in-rcs"></a>RCS'de Vergi Hesaplama'yı ayarlama

Bu bölümdeki adımlar belirli bir tüzel kişilikle ilişkili değildir. Bu yordamı yalnızca bir kez tamamlamanız gerekir ve RCS'deki herhangi bir tüzel kişilikte tamamlayabilirsiniz.

1. [RCS](https://marketing.configure.global.dynamics.com/)'de oturum açın
2. Finance'te **Elektronik raporlama** çalışma alanında, yeni bir yapılandırma sağlayıcısı ekleyin. Sağlayıcının adı olarak şirket adınızı kullanın. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Oluşturduğunuz yapılandırma sağlayıcısını seçin ve sonra **etkin olarak ayarla**'yı seçin.
4. **Microsoft** yapılandırma sağlayıcısını seçin ve ardından **depolar**'ı seçin.
5. **Tür** alanında **Genel**'i seçin.
6. **Aç**'ı seçin.
7. **Vergi Veri Modeli**'ne gidin, dosya ağacını genişletin ve ardından **Vergi Yapılandırması**'nı seçin.
8. En son sürümü seçin ve ardından **içe aktar**'ı seçin.
9. **Genelleştirme özellikleri (Önizleme)** çalışma alanına geri dönün, **Özellikler**'i seçin, **Vergi Hesaplama** kutucuğunu seçin ve sonra **Ekle**'yi seçin.
10. Aşağıdaki özellik türlerinden birini seçin:

    - **Yeni özellik** – Boş içeriğe sahip bir özellik ayarı oluşturun.
    - **Varolan özelliğe dayalı** – Varolan bir özellikten özellik oluşturun ve varolan özellik ayarından içeriği kopyalayın.

11. Özellik için bir ad ve açıklama girin ve **Özellik oluştur**'u seçin.

    Özellik oluşturulduktan sonra, otomatik olarak bir taslak sürümü oluşturulur.

12. Özelliğin taslak sürümünü seçin ve sonra **Düzenle**'yi seçin. **Vergi Hesaplama ayarı** sayfası doldurulur.
13. **Yapılandırma sürümü**'nü seçin. 8. adımda içe aktardığınız yapılandırma sürümünü görürsünüz.

    Microsoft, vergi hesaplama eklentisi için varsayılan bir vergi yapılandırması sağlar. Bu yapılandırma vergi hesaplama davranışlarına ilişkin gereksinimlerin çoğunu kapsar. Pazar görüşleri temel alınarak güncelleştirilecektir. Belirli gereksinimleri karşılamak üzere yapılandırmayı genişletmeniz gerekiyorsa, kendi vergi yapılandırmanızı nasıl oluşturacağınız ve seçebileceğiniz hakkında bilgi için [vergi hizmetinde uzantı oluşturma](./tax-service-add-data-fields-tax-integration-by-extension.md) konusuna bakın.

    **Yapılandırma sürümünü** seçtikten sonra birkaç ek sekme görüntülenir:

    - **Vergi kodları** – Bu sekme zorunludur. Vergi kodlarıyla ilgili ana verileri korumak için kullanılır. Tüzel kişilikteki vergi Özellik ayarının geçerli sürümünü etkinleştirdiğinizde, bu sekmede oluşturulan tüm vergi kodları Finance ile otomatik olarak eşitlenir.
    - **Vergi kodları uygulanabilirliği** – Bu sekme zorunludur. Vergi kodunu, vergi grubunu ve madde vergisi grubunu belirleyen bir matrisi tanımlamak için kullanılır. Belirlenen vergi kodu vergi tutarını hesaplamak için kullanılır. **Vergi kodu**, **vergi grubu** ve **Madde vergi grubu** alanlarının değerleri Finance'e döndürülür.
    - **Müşteri vergi kayıt numarası uygulanabilirliği**: Bu sekme isteğe bağlıdır. Bir müşteri için birden fazla vergi kayıt numaranız varsa, Vergi Hesaplama doğru vergi kayıt numarasını otomatik olarak belirleyebilir. Bu sekmedeki matriste, eklentinin belirleme işlemi için kullandığı kuralları tanımlarsınız. Aksi takdirde, Finance ve Supply Chain Management satış işlemleri için vergiye tabi belgelerde varsayılan vergi kayıt numarasını kullanmaya devam eder.
    - **Satıcı vergi kayıt numarası uygulanabilirliği**: Bu sekme isteğe bağlıdır. Bir satıcı için birden fazla vergi kayıt numaranız varsa, Vergi Hesaplama doğru vergi kayıt numarasını otomatik olarak belirleyebilir. Bu sekmedeki matriste, eklentinin belirleme işlemi için kullandığı kuralları tanımlarsınız. Aksi takdirde, Finance ve Supply Chain Management satın alma işlemleri için vergiye tabi belgelerde varsayılan vergi kayıt numarasını kullanmaya devam eder.
    - **Liste kodu uygulanabilirliği** – Bu sekme isteğe bağlıdır. Daha esnek ve yapılandırılabilir kurallarla **liste kodu** alanının değerinin otomatik olarak belirlenmesine yardımcı olabilir. Bu sekmedeki matriste, eklentinin belirleme işlemi için kullandığı kuralları tanımlayabilirsiniz. Aksi takdirde, Finance ve Supply Chain Management vergiye tabi belgelerde varsayılan kodu kullanmaya devam eder.

14. **Vergi kodları** sekmesinde, **Ekle**'yi seçin ve vergi kodunu ve bir açıklama girin.
15. **Vergi bileşenini** seçin. Vergi bileşeni, seçili vergi yapılandırmasının önceki sürümünde tanımlanmış bir yöntemler grubudur. Aşağıdaki vergi bileşenleri kullanılabilir:

    - Net tutara göre
    - Brüt tutara göre
    - Miktara göre
    - Marja göre
    - Vergi üzerinden vergi

16. **Kaydet**'i seçin. Seçtiğiniz vergi bileşeni esas alınarak daha fazla alan kullanılabilir hale gelir.
17. Vergi kodunun niteliğini tanımlamak için aşağıdaki seçenekleri kullanın:

    - Muaf
    - Kullanım vergisi
    - Karşı ödeme
    - Taban Tutar Hesaplamasından hariç tut

    Kullanım vergisi senaryosu için, pozitif vergi oranına sahip tek bir vergi kodu ayarlayın ve bunu **kullanım vergisi** olarak işaretleyin.

    Karşı ödeme senaryosu için, biri pozitif vergi oranına sahip olan ve diğeri negatif vergi oranına sahip ancak aynı fiyat değeri olan iki vergi kodu ayarlayın. Negatif vergi kodunu **Karşı ödeme** olarak işaretleyin. Finance'te karşı ödeme çözümü hakkında daha fazla bilgi için [KDV/GST düzenine ilişkin karşı ödeme mekanizmasına](emea-reverse-charge.md) bakın.
    
    Bazı ülkelerde gümrük vergisi gibi fiyat dahil işlemler için vergi matrahı hesaplamasında hariç tutulması gereken bazı vergi türleri için, **Taban Tutar Hesaplamasından Hariç Tut** onay kutusunu seçin.

    Bu vergi kodu için vergi oranlarını ve vergi tutarı sınırlarını koruyun.

18. Gerekli tüm diğer vergi kodlarını eklemek için 14 ile 17 arasındaki adımları yineleyin.
19. **Vergi kodları uygulanabilirliği** sekmesinde, doğru vergi kodunu belirlemek için gereken sütunları seçin ve ardından **Ekle**'yi seçin.
20. Her bir sütun için değerleri girin veya seçin. **Vergi kodu**, **vergi grubu** ve **Madde vergi grubu** alanları bu matrisin çıktısı olacaktır.
21. Müşteri vergi kayıt numaralarının, satıcı vergi kayıt numaralarının ve liste kodlarının uygulanabilirliğini ayarlamak için 19 ile 20 arasındaki adımları yineleyin.
22. **Kaydet**'i seçip sayfayı kapatın.
23. **Durumu değiştir** \> **Tamamla**'yı seçin. Durum **tamamlandı** olarak değiştirildikten sonra sürüm artık düzenlenemez.
24. **Durumu değiştir** \> **Yayınla**'yı seçin. Vergi özelliği ayarının bu sürümü genel depoya gönderilir ve Finance'te her yasal varlık için görünür olacaktır.

## <a name="dynamics-365-setup"></a>Dynamics 365'i ayarlama

RCS'deki ayarlamayı tamamladıktan sonra, önceki bölümde açıklandığı gibi vergi özelliğinin yayınlanmış bir sürümüne sahip olacaksınız. Finance'te Vergi Hesaplama'yı ayarlamak için bu adımları izleyin.

Bu bölümdeki ayarlama tüzel kişilik tarafından gerçekleştirilir. Finance'ta Vergi Hesaplama'yı etkinleştirmek istediğiniz her tüzel kişilik için yapılandırmalısınız.

1. Finance'ta, **Vergi** \> **Ayarla** \> **Vergi yapılandırması** \> **Vergi hesaplama ayarı (Önizleme)** bölümüne gidin.
2. **Genel** sekmesinde, aşağıdaki alanları ayarlayın:

    - **Vergi Hesaplama'yı Etkinleştir**: Tüzel kişilik için Vergi Hesaplama'yı etkinleştirmek üzere bu onay kutusunu işaretleyin. Geçerli tüzel kişilik için etkinleştirilmemişse, tüzel kişilik vergiyi belirlemek ve hesaplamak için mevcut vergi altyapısını kullanmaya devam eder.
    - **Özellik ayarı**: Tüzel kişilik için yayınlanmış bir vergi özelliği ayarı ve sürümü seçin. Yayınlanmış bir vergi özelliğini ayarlama ve tamamlama hakkında daha fazla bilgi için, bu konunun önceki bölümüne bakın.
    - **İş Süreci** – Etkinleştirilecek iş süreçlerini seçin.
    - **Vergi kodu ayarlamasını Etkinleştir**: Satış vergisi sayfasında vergi kodu ayarlamalarını etkinleştirmek için bu seçeneği **Evet** olarak ayarlayın.

3. **Hesaplama** sekmesinde, tüzel kişilik için beklenen yuvarlama kuralını tanımlayın.
4. **Hata işleme** sekmesinde, tüzel kişilik için beklenen hata işleme yöntemini tanımlayın. Her sonuç kodu için üç seçenek vardır:

    - No
    - Uyarı
    - Hata

5. Ayarı kaydedin.
6. Her ek tüzel kişilik için 1 ile 5 arasındaki adımları yineleyin.

## <a name="transaction-processing"></a>İşlem işleme

Tüm ayarlama yordamlarını tamamladıktan sonra, Finance'te vergiyi belirlemek ve hesaplamak için Vergi Hesaplama'yı kullanabilirsiniz. İşlemleri işleme adımları aynı kalır. Aşağıdaki işlemler Finance sürüm 10.0.18'de desteklenmektedir:

- Satış işlemi

    - Satış teklifi
    - Satış siparişi
    - Onay
    - Malzeme çekme listesi
    - Sevk irsaliyesi
    - Satış faturası
    - Alacak dekontu
    - Sipariş iadesi
    - Masraf başlığı
    - Satır masrafı

- Satın alma işlemi

    - Satın alma siparişi
    - Onay
    - Giriş listesi
    - Ürün girişi
    - Satınalma faturası
    - Masraf başlığı
    - Satır masrafı
    - Alacak dekontu
    - Sipariş iadesi
    - Satınalma talebi
    - Satın alma talebi satır masrafı
    - Teklif talebi
    - Teklif talebi başlık masrafı
    - Teklif talebi satır masrafı

- Stok işlemi

    - Transfer emri - sevk
    - Transfer emri - al
