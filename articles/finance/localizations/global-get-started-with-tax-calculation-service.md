---
title: Vergi Hesaplamayı kullanmaya başlama
description: Bu konuda, Vergi Hesaplamasının nasıl ayarlanacağı açıklanmaktadır.
author: wangchen
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1ddbb22d4f7c6108ca93b415276c53794b5450dd
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394524"
---
# <a name="get-started-with-tax-calculation"></a>Vergi Hesaplamayı kullanmaya başlama

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Bu konu, Vergi Hesaplama'yı kullanmaya başlama hakkında bilgi sağlar. Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS), Dynamics 365 Finance ve Dynamics 365 Supply Chain Management içindeki yapılandırma adımlarını izlemeniz konusunda yol gösterir. Daha sonra, Finance ve Supply Chain Management işlemlerinde Vergi Hesaplama özelliklerinin kullanımıyla ilgili genel işlemi inceler.

Ayarlama dört ana adımdan oluşur:

1. LCS'de Vergi Hesaplama eklentisini yükleyin.
2. RCS'de, Vergi Hesaplama özelliğini ayarlayın. Bu ayar bir tüzel kişiliğe özgü değildir. Finance ve Supply Chain Management tüzel kişileri arasında paylaşılabilir.
3. Finance ve Supply Chain Management'ta tüzel kişiliğe göre Vergi Hesaplama parametrelerini ayarlayın.
4. Finance ve Supply Chain Management'ta satış siparişleri gibi işlemler oluşturun ve vergileri belirlemek ve hesaplamak için Vergi Hesaplama eklentisini kullanın.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki yordamları tamamlamadan önce her ortam türü için önkoşulların yerine getirilmesi gerekir.

### <a name="for-a-production-environment"></a>Üretim ortamı için

Üretim ortamı için aşağıdaki önkoşulların karşılanması gerekir:

- LCS hesabınıza erişiminizin ve Dynamics 365 sürüm 10.0.21 veya sonrasını çalıştıran bir Katman 2 ya da üstü ortam bulunan dağıtılmış bir LCS projenizin olması gerekir.
- Kuruluşunuz için bir RCS ortamı oluşturmanız ve hesabınıza erişebilmeniz gerekir. RCS ortamı oluşturma hakkında daha fazla bilgi için bkz. [Regulatory Configuration Service'e Genel Bakış](rcs-overview.md).
- İş gereksinimlerinize bağlı olarak, dağıttığınız Finance veya Supply Chain Management ortamının **Özellik yönetimi** çalışma alanında aşağıdaki özelliklerin açık olması gerekir:

    - Vergi Hesaplama
    - Birden çok KDV sicil numarasını destekle
    - Transfer emrindeki vergi
    - Yalnızca vergi işlemlerine dayalı AB satış listesi transferi
    - Birden Fazla Vergi Koduna göre intrastat raporlama
    - Birden Fazla Vergi Koduna göre AB Satış listesi raporlaması
    - Birden Fazla Vergi Koduna göre satış vergisi beyannamesi

- Dağıttığınız RCS ortamının **Özellik yönetimi** çalışma alanında aşağıdaki özelliklerin açık olması gerekir.

    - Globalleştirme özellikleri

### <a name="for-a-test-environment-public-preview"></a>Test ortamı için (Genel Önizleme)

Test ortamı için aşağıdaki önkoşulların karşılanması gerekir:

- LCS hesabınıza erişiminizin ve KB4616360 özellikli Dynamics 365 sürüm 10.0.18 veya sonraki bir sürümü çalıştıran bir Katman 2 ya da üstü ortam bulunan dağıtılmış bir LCS projenizin olması gerekir.
- Kuruluşunuz için bir RCS ortamı oluşturmanız ve hesabınıza erişebilmeniz gerekir. RCS ortamı oluşturma hakkında daha fazla bilgi için bkz. [Regulatory Configuration Service'e Genel Bakış](rcs-overview.md).
- Dağıttığınız Finance veya Supply Chain Management ortamında denemeyi etkinleştirmek için <taxcalc@microsoft.com> adresine e-posta göndererek Microsoft'a başvurmanız gerekir.
- İş gereksinimlerinize bağlı olarak, dağıttığınız Finance veya Supply Chain Management ortamının **Özellik yönetimi** çalışma alanında aşağıdaki özelliklerin açık olması gerekir:

    - Vergi Hesaplama
    - Birden çok KDV sicil numarasını destekle
    - Transfer emrindeki vergi
    - Yalnızca vergi işlemlerine dayalı AB satış listesi transferi
    - Birden Fazla Vergi Koduna göre intrastat raporlama
    - Birden Fazla Vergi Koduna göre AB Satış listesi raporlaması
    - Birden Fazla Vergi Koduna göre satış vergisi beyannamesi

- Dağıttığınız RCS ortamının **Özellik yönetimi** çalışma alanında aşağıdaki özelliklerin açık olması gerekir.

    - Globalleştirme özellikleri

## <a name="set-up-tax-calculation-in-lcs"></a>LCS'de Vergi Hesaplama'yı ayarlama

1. [LCS'te](https://lcs.dynamics.com) oturum açın
2. Microsoft Power Platform tümleştirmesi için kurulumu tamamlayın. Daha fazla bilgi için bkz. [Eklentiler sekmesi](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Dağıttığınız ortamlardan birini seçin ve ardından **Yeni eklenti yükle** seçeneğini belirleyin.
4. **Vergi Hesaplama**'yı seçin.
5. Hüküm ve koşulları okuyup kabul edin ve sonra **Yükle**'yi seçin.

## <a name="set-up-tax-calculation-in-rcs"></a>RCS'de Vergi Hesaplama'yı ayarlama

Bu bölümdeki adımlar belirli bir tüzel kişilikle ilişkili değildir. Bu yordamı yalnızca bir kez tamamlamanız gerekir ve RCS'deki herhangi bir tüzel kişilikte tamamlayabilirsiniz.

1. [RCS](https://marketing.configure.global.dynamics.com/)'de oturum açın
2. **Elektronik raporlama** çalışma alanında, yeni bir yapılandırma sağlayıcısı ekleyin. Sağlayıcının adı olarak şirket adınızı kullanın. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Oluşturduğunuz yapılandırma sağlayıcısını seçin ve sonra **etkin olarak ayarla**'yı seçin.
4. **Microsoft** yapılandırma sağlayıcısını seçin ve ardından **depolar**'ı seçin.
5. **Tür** alanında **Genel**'i seçin.
6. **Aç**'ı seçin.
7. **Vergi Veri Modeli**'ne gidin, dosya ağacını genişletin ve ardından **Vergi Yapılandırması**'nı seçin.
8. Finance sürümünüze bağlı olarak, doğru vergi yapılandırması sürümünü seçin ve ardından **İçeri Aktar** seçeneğini belirleyin.

    | Yayım sürümü | Vergi konfigürasyonu                       | Model eşleme                   |
    | --------------- | --------------------------------------- | ------------------------------- |
    | 10.0.18         | Vergi Yapılandırması - Avrupa 30.12.82     |                                 |
    | 10.0.19         | Vergi Hesaplama Yapılandırması 36.38.193 |                                 |
    | 10.0.20         | Vergi Hesaplama Yapılandırması 40.43.208 |                                 |
    | 10.0.21         | Vergi Hesaplama Yapılandırması 40.46.212 | Dataverse Model Eşlemesi 40.46.9 |

9. **Genelleştirme özellikleri** çalışma alanında, **Özellikler**'i seçin, **Vergi Hesaplaması** kutucuğunu ve ardından **Ekle** seçeneğini belirleyin.
10. Aşağıdaki özellik türlerinden birini seçin:

    - **Yeni özellik** – Boş içeriğe sahip bir özellik ayarı oluşturun.
    - **Varolan özelliğe dayalı** – Varolan bir özellikten özellik oluşturun ve varolan özellik ayarından içeriği kopyalayın.

11. Özellik için bir ad ve açıklama girin ve **Özellik oluştur**'u seçin.

    Özellik oluşturulduktan sonra, otomatik olarak bir taslak sürümü oluşturulur. Tamamlanan sürümlerde taslak sürümü yeniden temellendirmek için **Bu sürümü al**'ı seçebilirsiniz.

12. Özelliğin taslak sürümünü seçin ve sonra **Düzenle**'yi seçin. **Vergi Hesaplama ayarı** sayfası doldurulur.
13. **Yapılandırma sürümü**'nü seçin. 8. adımda içe aktardığınız yapılandırma sürümünü görürsünüz.

    Microsoft, vergi hesaplama için varsayılan bir vergi yapılandırması sağlar. Bu yapılandırma vergi hesaplama davranışlarına ilişkin gereksinimlerin çoğunu kapsar. Pazar görüşleri temel alınarak güncelleştirilecektir. Belirli gereksinimleri karşılamak üzere yapılandırmayı genişletmeniz gerekiyorsa, kendi vergi yapılandırmanızı nasıl oluşturacağınız ve seçebileceğiniz hakkında bilgi için [vergi hizmetinde uzantı oluşturma](./tax-service-add-data-fields-tax-integration-by-extension.md) konusuna bakın.

14. **Yapılandırma sürümü**'nü seçtikten sonra birkaç ek sekme görüntülenir. Zorunlu sekme kurulumunu tamamlamak için burada gösterilen sırayı izleyin.

    **Zorunlu kurulum**

    - **Vergi kodları**: Vergi kodları için ana verileri koruyun. Geçerli sürümü etkinleştirdiğinizde bu sekmede oluşturulan tüm vergi kodları Finance ile otomatik olarak eşitlenir.
    - **Vergi grubu**: Vergi grubu ana verilerini ve grubun altındaki vergi kodlarını tanımlayın.
    - **Madde vergisi grubu**: Madde vergisi grubu ana verilerini ve grubun altındaki vergi kodlarını tanımlayın.

    **İsteğe bağlı kurulum**

    - **Vergi grubu uygulanabilirliği**: Vergi grubunu belirleyen bir matris tanımlayın. Bu matristeki uygulanabilirlik kuralları, Dynamics 365'teki vergiye tabi belge ile eşleşmezse Vergi Hesaplama, vergiye tabi belge satırındaki varsayılan değeri kullanır.
    - **Madde vergisi grubu uygulanabilirliği**: Madde vergisi grubunu belirleyen bir matris tanımlayın. Bu matristeki uygulanabilirlik kuralları, Dynamics 365'teki vergiye tabi belge ile eşleşmezse Vergi Hesaplama, vergiye tabi belge satırındaki varsayılan değeri kullanır.
    - **Müşteri vergi kayıt numarası uygulanabilirliği**: Bir müşteri için birden fazla vergi kayıt numaranız varsa Vergi Hesaplama, doğru vergi kayıt numarasını otomatik olarak belirleyebilir. Bu sekmedeki matriste, belirleme işlemi için kullanılması gereken kuralları tanımlayın. Aksi takdirde, Finance ve Supply Chain Management satış işlemleri için vergiye tabi belgelerde varsayılan vergi kayıt numarasını kullanmaya devam eder.
    - **Satıcı vergi kayıt numarası uygulanabilirliği**: Bir satıcı için birden fazla vergi kayıt numaranız varsa Vergi Hesaplama, doğru vergi kayıt numarasını otomatik olarak belirleyebilir. Bu sekmedeki matriste, belirleme işlemi için kullanılması gereken kuralları tanımlayın. Aksi takdirde, Finance ve Supply Chain Management satın alma işlemleri için vergiye tabi belgelerde varsayılan vergi kayıt numarasını kullanmaya devam eder.
    - **Liste kodu uygulanabilirliği**: Daha esnek ve yapılandırılabilir kurallarla **Liste kodu** alanının değerini otomatik olarak belirleyin. Bu sekmedeki matriste, belirleme işlemi için kullanılması gereken kuralları tanımlayın. Aksi takdirde, Finance ve Supply Chain Management vergiye tabi belgelerde varsayılan kodu kullanmaya devam eder.

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
    - Taban tutar hesaplamasından hariç tutma

    Kullanım vergisi senaryosu için pozitif vergi oranına sahip tek bir vergi kodu ayarlayın ve bunu **Kullanım vergisi** olarak işaretleyin.

    Karşı ödeme senaryosu için, biri pozitif vergi oranına sahip olan ve diğeri negatif vergi oranına sahip ancak aynı fiyat değeri olan iki vergi kodu ayarlayın. Negatif vergi kodunu **Karşı ödeme** olarak işaretleyin. Finance'te karşı ödeme çözümü hakkında daha fazla bilgi için [KDV/GST düzenine ilişkin karşı ödeme mekanizmasına](emea-reverse-charge.md) bakın.

    Fiyat dahil işlemlerde (örneğin, bazı ülkelerde veya bölgelerde gümrük vergisi) vergi matrahının hesaplanmasından hariç tutulması gereken bazı vergi türleri için **Taban Tutar Hesaplamasından Hariç Tut** onay kutusunu seçin. Bu parametre hakkında daha fazla bilgi için bkz. [Vergi dahil Fiyat etkinleştirildiğinde fiyatın üzerine vergi hesaplama](global-exclude-from-tax-base-amount-calculation.md).

    Bu vergi kodu için vergi oranlarını ve vergi tutarı sınırlarını koruyun.

18. Gerekli tüm diğer vergi kodlarını eklemek için 14 ile 17 arasındaki adımları yineleyin.
19. **Vergi grubu** sekmesinde, **Vergi grubu** sütununu seçin, bunu giriş koşulu olarak matrise ekleyin ve ardından vergi grubu ana verilerini korumak için satırlar ekleyin.

    Aşağıda bir örnek verilmiştir.

    | Vergi grubu    | Vergi kodları           |
    | ------------ | ------------------- |
    | DEU_Domestic | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Domestic | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

20. **Madde vergisi grubu** sekmesinde, **Madde vergisi grubu** sütununu seçin, bunu giriş koşulu olarak matrise ekleyin ve ardından madde vergisi grubu ana verilerini korumak için satırlar ekleyin.

    Aşağıda bir örnek verilmiştir.

    | Madde vergisi grubu | Vergi kodları                                    |
    | -------------- | -------------------------------------------- |
    | Dolu           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Exempt |
    | Düşürüldü        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

21. **Vergi grubu uygulanabilirliği** sekmesinde, doğru vergi grubunu belirlemek için gereken sütunları seçin ve ardından **Ekle** seçeneğini belirleyin. Her bir sütun için değerleri girin veya seçin. **Vergi grubu** alanı, bu matrisin çıkışı olacaktır. Bu sekme yapılandırılmadıysa hareket satırındaki satış vergisi grubu kullanılır.

    Aşağıda bir örnek verilmiştir.

    | İş süreci | Sevk çıkış yeri | Sevk varış yeri | Vergi grubu    |
    | ---------------- | --------- | ------- | ------------ |
    | Satışlar            | DEU       | DEU     | DEU_Domestic |
    | Satışlar            | DEU       | FRA     | DEU_EU       |
    | Satışlar            | BEL       | BEL     | BEL_Domestic |
    | Satışlar            | BEL       | FRA     | BEL_EU       |

22. **Madde vergisi grubu uygulanabilirliği** sekmesinde, doğru vergi kodunu belirlemek için gereken sütunları seçin ve ardından **Ekle** seçeneğini belirleyin. Her bir sütun için değerleri girin veya seçin. **Madde vergisi grubu** alanı, bu matrisin çıkışı olacaktır. Bu sekme yapılandırılmadıysa hareket satırındaki madde satış vergisi grubu kullanılır.

    Aşağıda bir örnek verilmiştir.

    | Madde kodu | Madde vergisi grubu |
    | --------- | -------------- |
    | D0001     | Dolu           |
    | D0003     | Düşürüldü        |

    Vergi kodlarının Vergi Hesaplama'da nasıl belirlendiği hakkında daha fazla bilgi için bkz. [Satış vergisi grubu ve madde satış vergisi grubu belirleme mantığı](global-sales-tax-group-determination.md).

23. İş gereksinimlerine bağlı olarak, müşteri vergi kayıt numaralarının, satıcı vergi kayıt numaralarının ve liste kodlarının uygulanabilirliğini ayarlayın.
24. **Kaydet**'i seçip sayfayı kapatın.
25. **Durumu değiştir** \> **Tamamla**'yı seçin. Durum **tamamlandı** olarak değiştirildikten sonra sürüm artık düzenlenemez.
26. **Durumu değiştir** \> **Yayınla**'yı seçin. Vergi özelliği ayarının bu sürümü genel depoya gönderilir ve Finance'te her yasal varlık için görünür olacaktır.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Dynamics 365'te Vergi Hesaplama'yı ayarlama

RCS'deki kurulum tamamlandıktan sonra vergi özelliğinin yayınlanmış bir sürümüne sahip olursunuz. Finance'te Vergi Hesaplama'yı ayarlamak için bu adımları izleyin.

Bu bölümdeki ayarlama tüzel kişilik tarafından gerçekleştirilir. Finance'ta Vergi Hesaplama'yı etkinleştirmek istediğiniz her tüzel kişilik için yapılandırmalısınız.

1. Finance'te, **Vergi** \> **Kurulum** \> **Vergi yapılandırması** \> **Vergi hesaplama parametreleri**'ne gidin.
2. **Genel** sekmesinde, aşağıdaki alanları ayarlayın:

    - **Vergi Hesaplama Hizmetini Etkinleştir**: Tüzel kişilik için Vergi Hesaplama'yı etkinleştirmek üzere bu onay kutusunu işaretleyin. Geçerli tüzel kişilik için etkinleştirilmemişse, tüzel kişilik vergiyi belirlemek ve hesaplamak için mevcut vergi altyapısını kullanmaya devam eder.
    - **Özellik ayarı**: Tüzel kişilik için yayınlanmış bir vergi özelliği ayarı ve sürümü seçin. Yayınlanmış bir vergi özelliğini ayarlama ve tamamlama hakkında daha fazla bilgi için, bu konunun önceki bölümüne bakın.
    - **İş Süreci** – Etkinleştirilecek iş süreçlerini seçin.

3. **Hesaplama** sekmesinde, tüzel kişilik için beklenen yuvarlama kuralını tanımlayın. Yuvarlama mantığı hakkında daha fazla bilgi için bkz. [Vergi hesaplama yuvarlama kuralları](https://go.microsoft.com/fwlink/?linkid=2166988).
4. **Hata işleme** sekmesinde, tüzel kişilik için beklenen hata işleme yöntemini tanımlayın. Kullanılabilir üç seçenek vardır:

    - No
    - Uyarı
    - Hata

    **Ayrıntılar** bölümünde her sonuç kodu için bir hata işleme yöntemi ayarlayabilirsiniz. Alternatif olarak, bazı sonuç kodları, vergi hesaplama hizmetiyle eşitlenmezse **Genel** bölümünde varsayılan bir yöntem ayarlayabilirsiniz.

5. **Çoklu KDV kaydı** sekmesinde, çoklu KDV kayıtları senaryosu altında çalışmak için KDV beyannamesi, AB Satış Listesi ve İntrastat'ı ayrı ayrı açabilirsiniz. Çoklu KDV kayıtlarına yönelik vergi raporlama hakkında daha fazla bilgi için bkz. [Birden çok KDV kaydı için raporlama](emea-reporting-for-multiple-vat-registrations.md).
6. Kurulumu kaydedin ve her ek tüzel kişilik için önceki adımları yineleyin. Yeni bir sürüm yayımlandığında ve bunu uygulamak istediğinizde **Vergi hesaplama parametreleri** sayfasının **Genel** sekmesindeki **Özellik kurulumu** alanını ayarlayın (bkz. adım 2).

## <a name="transaction-processing"></a>İşlem işleme

Tüm ayarlama yordamlarını tamamladıktan sonra Finance'te vergiyi belirleyip hesaplamak için Vergi Hesaplama'yı kullanabilirsiniz. İşlemleri işleme adımları aynı kalır. Aşağıdaki işlemler Finance sürüm 10.0.21'de desteklenmektedir:

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
