---
title: Elektronik faturalamayı eklentisini kurma
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management uygulamalarında elektronik faturalama eklentisinin nasıl kurulacağını açıklamaktadır.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 92ffd2076497325fb986478328c4b2584929881d
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2020
ms.locfileid: "3836052"
---
# <a name="set-up-the-electronic-invoicing-add-on"></a>Elektronik faturalamayı eklentisini kurma

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Elektronik faturalama eklenti özelliğinin kurulumu, gerekli yapılandırmayı Regulatory Configuration Services (RCS) ortamı aracılığıyla oluşturma ve bu yapılandırmayı elektronik faturalama eklenti sunucusunda yayımlama işlemidir. Kurulum, elektronik faturalama eklentisinin Internet üzerinden bir üçüncü taraf varlıkla Web Hizmetleri aracılığıyla iletişim kurup veri alışverişi yapmak için güvenli bir protokol kullanmasını sağlayan yapılandırılabilir kurallar oluşturmanıza olanak sağlar.

Yapılandırılabilirlik, dijital dosyalar üzerinden gönderilen ve alınan içeriği oluşturmak amacıyla elektronik raporlama (ER) biçimi yapılandırmasına bağlıdır. Ayrıca, kod yazmanızı gerektirmeden, üçüncü taraf Web hizmetlere yanıtları göndermek ve bu hizmetlerden yanıt almak için iletişim eylemlerinin düzenlemesine dayanır.

## <a name="overview"></a>Genel bakış

"Elektronik faturalama eklentisi özelliği", Elektronik faturalama eklenti sunucusunu kullanmak üzere yapılandırılmış ve yayımlanmış olan kaynağın genel adıdır. Özellik kurulumu, başka şeylerin yanı sıra, yapılandırılabilir dışarı aktarma ve içe aktarma dosyaları oluşturmak için ER yapılandırma biçimlerinin kullanılması ve isteklerin gönderilmesi, yanıtları içe aktarmak ve yanıt içeriğini ayrıştırmaya olanak tanıyan eylemleri ve eylem akışlarının kullanımını birleştirir.

Aşağıdaki şekil, Elektronik faturalama eklentisi özelliğinin ana bileşenlerini gösterir.

![Elektronik faturalama eklentisi özelliğine genel bakış](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

Fatura biçimlerindeki ve eylem akışlarındaki çeşitlilikler nedeniyle, özellik kurulumu ülkeye veya bölgeye veya iş gereksinimlerine göre değişebilir.

## <a name="set-up-the-electronic-invoicing-add-on-feature"></a>Elektronik faturalama eklenti özelliğini kurma

Kurulum işleminin RCS ortamınızda tamamlanması gereklidir. Yeni bir elektronik faturalama eklenti özelliği oluşturmak için aşağıdaki adımları izleyin.

1. RCS ortamınızda oturum açın.
2. **Genelleştirme özellikleri** çalışma alanında, **Özellikler** bölümünde, **Elektronik faturalama eklentisi** kutucuğunu seçin.
3. **Elektronik faturalama eklenti özellikleri** sayfasında, Genel depodan ER veri modeli yapılandırmasını içe aktarmak için **İçe aktar**'ı seçin.
4. Elektronik faturalama eklentisi özelliği oluşturmak için **Ekle**'yi seçin. Özelliği sıfırdan oluşturabilir veya var olan bir elektronik faturalama eklentisi özelliğinden türetebilirsiniz.

    ![Elektronik faturalama eklentisi özelliği ekleme](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> Yeni bir elektronik faturalama eklenti özelliği oluşturduğunuzda, bir sürüm numarası vardır ve varsayılan durumu **Taslak** olarak ayarlanır.

### <a name="configurations"></a>Konfigürasyonlar

Yapılandırmalar dönüştürmeler için gerekli olan ve üçüncü taraf Web hizmetleriyle iletişim sırasında alışverişi yapılan dosyaları oluşturan ER biçim yapılandırmalarını tutar. Elektronik faturalama eklenti özelliği, Web servis sağlayıcısı tarafından sağlanan tümleştirme teknik belirtimine bağlı olarak, gereken sayıda ER dosya biçimi yapılandırmasına sahip olabilir.

Elektronik faturalama eklenti özelliğine ER biçimleri eklemek için aşağıdaki adımları izleyin.

1. Elektronik faturalama eklentisi özelliği için, **Elektronik faturalama eklentisi özellikleri** sayfasında, ER dosya biçimi yapılandırması eklemek için, **Yapılandırmalar** sekmesinde **Ekle**'yi seçin.

    ![Elektronik faturalama eklentisi özelliği yapılandırmalarını ekleme](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Sıfırdan bir Elektronik faturalama eklenti özelliği oluşturduğunuzda, tüm ER dosya biçimi yapılandırmalarını el ile eklemeniz gerekir. Var olan bir özellikten Elektronik faturalama eklenti özelliği türettiğinizde, özgün elektronik faturalama eklentisi özelliğinden devralındığından, ER dosya biçimi yapılandırmaları otomatik olarak oluşturulur.

2. ER dosya biçimi yapılandırmasını düzenleyebileceğiniz **Biçim tasarımcısı** sayfasını açmak için **Düzenle** seçin.

    ![Elektronik faturalama eklentisi özelliği yapılandırmalarını düzenleme](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Biçimi düzenlerken, yapılandırma sürümünün durumu **Taslak** olarak ayarlanır.

3. **Biçim tasarımcısı** sayfasını, dosya biçimi yapılandırmasını değiştirmek için kullanın. Daha fazla bilgi için bkz. [Elektronik belge yapılandırmalarını oluşturma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Biçim tasarımcısı sayfası](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>Özellik kurulumları

Özellik kurulumları, üçüncü taraf bir Web hizmetiyle ilgili iletişim ve güvenlik kurallarını içerir. Elektronik faturalama eklenti özelliği, gerçekleştirmek istediğiniz iş kuralına bağlı olarak, gereken sayıda özellik kurulumu içerebilir.

Elektronik faturalama eklenti özelliğine özellik kurulumlarını eklemek için aşağıdaki adımları izleyin.

1. Elektronik faturalama eklentisi özelliğine özellik kurulumlarını eklemek için, **Elektronik faturalama eklentisi özellikleri** sayfasında **Kurulumlar** sekmesinde **Ekle**'yi seçin.

    ![Elektronik faturalama eklentisi özelliği kurulumlarını ekleme](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > Sıfırdan bir Elektronik faturalama eklenti özelliği oluşturduğunuzda, gereksinim duyduğunuz tüm özellik kurulumlarını el ile eklemeniz gerekir. Var olan bir özellikten Elektronik faturalama eklenti özelliği türettiğinizde, özgün elektronik faturalama eklentisi özelliğinden devralındığından, tüm özellik kurulumları otomatik olarak oluşturulur.

2. Özellik sürümü kurulumunu düzenlemek için **Düzenle** öğesini seçin.

    ![Elektronik faturalama eklentisi özelliği kurulumlarını düzenleme](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. Eylemleri, uygulanabilirlik kurallarını ve değişkenleri yapılandırmak için **Özellik sürümü kurulumu** sayfasını kullanın.

    ![Eylemler, uygulanabilirlik kuralları ve değişkenler](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>Eylemler

Eylemler, sıralı olarak çalışan, önceden tanımlanmış bir operasyonlar listesidir. Bu liste, Elektronik faturalama eklentisi özelliğinin tam yürütülmesi için gereken adımların dökümünü gösterir. Eylemler, aynı elektronik faturalama ek bileşeni ile iletişimi her iki yönde de kapsülleyebilirsiniz: bir hedef için istek gönderme, yanıt alma ve içeriğini ayrıştırma.

Her eylem, eylemin amacını yerine getirmek için gerekli olan parametrelerin önceden tanımlı bir listesini içerir. Ek parametreler isteğe bağlı olarak sağlanabilir.

#### <a name="actions-fasttab"></a>İşlevler hızlı sekmesi

**Özellik sürümleri kurulumu** sayfasında, **Eylemler** sekmesinde, **Eylemler** hızlı sekmesinde, eylemleri yönetmek için bu adımların birini veya her ikisini birden izleyin:

- Yeni eylemler eklemek veya var olan eylemleri silmek için **Yeni** veya **Sil**'i seçin.
- Seçili eylemleri kılavuzda aşağı veya yukarı taşımak için **Yukarı** veya **Aşağı**'yı seçin ve böylece çalıştıkları sırayı değiştirin. Eylemler, kılavuzda göründükleri sırada, üstten alta doğru çalıştırılır.

![Eylemleri yönetme](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

Aşağıdaki tabloda, **Eylemler** hızlı sekmesinde kullanılabilecek alanlar açıklanmaktadır.

| Alan        | Tanım |
|--------------|-------------|
| Eylem       | Önceden tanımlanmış sekiz eylem vardır:<ul><li><strong>Belgeyi imzala</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>Belgeyi dönüştür</strong></li><li><strong>Yanıtı işle</strong></li><li><strong>REST Web servisini çağır</strong></li><li><strong>Meksika PAC hizmetini çağır</strong></li><li><strong>Brezilya SEFAZ hizmetini çağır</strong></li><li><strong>İtalya SDI hizmetini çağır</strong></li></ul> |
| Eylem adı  | Eylemin adı ve yürütme sırası. |
| Tanım  | Eylemin tanımı. |
| Yeniden denemeyi etkinleştir | Seçili bir onay kutusu, önceki girişim başarısız olduğunda eylemin yeniden deneneceği anlamına gelir. |
| Yeniden deneme eylemi | Yeniden deneme durumunda, yeniden denemenin başlayacağı eylem. Böylece yeniden deneme geçerli eylemle sona erer (yeniden denenecek eylem dahil). Bunları içeren eylemler için, **En az geri alma** ve **En fazla geri alma** parametresi sayısı, en az ve en fazla yeniden deneme sayısını belirtir. |

#### <a name="parameters-fasttab"></a>Parametreler hızlı sekmesi

**Parametreler** hızlı sekmesi, **Eylemler** hızlı sekmesinde seçili olan eyleme ait parametreleri listeler.

![Parametreler hızlı sekmesi](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

Aşağıdaki tabloda, **Parametreler** hızlı sekmesinde kullanılabilecek alanlar açıklanmaktadır.

| Alan       | Tanım |
|-------------|-------------|
| Dosya Adı        | Önceden tanımlanmış bir parametreler listesi. Daha fazla bilgi için bkz. [Eyleme göre parametreler listesi](#list-of-parameters-by-action). |
| Tanım | Parametre açıklaması. |
| Değer       | Parametrenin değeri. |

#### <a name="list-of-parameters-by-action"></a>Eyleme göre parametre listesi

Kullanılabilir parametreler, **Eylemler** hızlı sekmesinde seçilen eyleme göre farklılık gösterir.

###### <a name="action-sign-document"></a>Eylem: belgeyi imzalama

| Parametre                             | Tanım |
|---------------------------------------|-------------|
| Giriş dosyası                            | Elektronik imza kullanılarak imzalanması gereken giriş XML belgesi dosyası. |
| Sertifika adı                      | Sertifikanın depolama alanındaki adı. |
| İmza tipi                        | Kullanılacak imzanın türü. |
| İmza yöntemi adı                 | Elektronik imza oluşturmak için kullanılan imza yönteminin adı. |
| Özet yöntem adı                    | Dijital imzada özet dize oluşturmak için kullanılan özet yöntemi. |
| Kurallaştırma yöntemi adı          | İmza karmasının hesaplanmasında kullanılan kurallaştırma yöntem türü. |
| Referans öznitelik adı              | Referans kodunun imza öğesine eklenmesi gereken konumu gösteren öznitelik adı. |
| İmzalanacak öğenin adı               | Elektronik imza kullanılarak imzalanması gereken belgedeki XML öğesinin adı. Hiçbir öğe belirtilmezse, belgenin kökü imzalanır. |
| İmza eklenecek öğenin adı   | Oluşturulan dijital imzanın ekleneceği XML öğesinin adı. Hiçbir öğe belirtilmezse, imza belgenin köküne eklenir. |
| XLST dosyası özet dönüşümü       | Elektronik imza için özet dize oluşturmak amacıyla özet dönüştürme kurallarını içeren Genişletilebilir Stil Sayfası Dili Dönüşümleri (XSLT) dosyası. |
| Özet dize ekleme yolu          | Oluşturulan özet dizenin ekleneceği konumun **\<elementName\>.\<Attribute.Path\>** biçimindeki yolu. |
| Sertifika numarası konumu           | Sertifika numarasının yerleştirileceği öğenin ve özniteliğin adı. |
| Sertifika verilerinin konumu          | Sertifika verilerinin (Base64) yerleştirilmesi gereken öğenin ve özniteliğin adı. |
| Sertifika numarası ASCII biçimindedir | Sertifikanın numarasının ASCII biçiminde kodlanmış olup olmadığını belirten bir değer. |

###### <a name="action-filestoreactionname"></a>Eylem: FileStoreActionName

| Parametre  | Tanım |
|------------|-------------|
| Giriş dosyası | Depolanacak giriş dosyası. |

###### <a name="action-transform-document"></a>Eylem: Belgeyi dönüştür

| Parametre                       | Tanım |
|---------------------------------|-------------|
| Giriş dosyası                      | Eylem için çalıştırılması gereken verileri sağlayan kaynak dosya. |
| Yön                       | İçe aktarma biçiminin mi yoksa dışa aktarma biçiminin mi kullanılacağını belirten bir değer. |
| Konfigürasyon kodu                | Çalıştırılması gereken biçim. |
| Yapılandırma sürümü           | Herhangi bir yapılandırma sürümü belirtilmezse, en son sürüm kullanılacaktır. |
| Yapılandırma tümleştirme noktası | Raporlama çalışma zamanına veri sağlayan kaynak dosya. |

###### <a name="action-process-response"></a>Eylem: Yanıtı işle

| Parametre                    | Tanım |
|------------------------------|-------------|
| Giriş dosyası                   | Çözümlenecek yanıt. |
| Raporlama yapılandırması listesi | Yanıtları ayrıştırmak için kullanılan yapılandırmaların listesi. |

###### <a name="action-call-rest-web-service"></a>Eylem: REST Web servisini çağır

| Parametre                   | Tanım |
|-----------------------------|-------------|
| Web hizmeti URL'si             | İsteklerin gönderileceği URL. |
| Web isteği zaman aşımı         | Web hizmeti yanıtı için beklenecek en uzun süre (milisaniye cinsinden). |
| İstek işlemi türü      | HTTP istek işleminin türü (örneğin, **GET**, **POST**veya **DELETE**). |
| Sertifika adları           | Sertifika adları. |
| Yanıt gövdesi kodlaması      | HTTP yanıt gövdesinin beklenen kodlamasıdır, böylece kodu doğru şekilde çözümlenebilir. |
| HTTP isteği içerik türü   | HTTP isteği içerik türü üstbilgi girişi. |
| HTTP isteği içerik gövdesi   | HTTP isteği gövdesi. (Gövde boş bırakılabilir.) |
| HTTP parametre sorgusu değerleri | URL'yi değişken parametrelerle doldurmak için kullanılan parametre sorgu değerleri. |
| İstek rotası               | HTTP isteğine ilişkin yol rotası. Değişken parametreleri **\{paramName\}** gösteriminde yazılabilir. Örnek: **"api/{id}/submit"**. |
| Rota parametre listesi        | Rotaya değişkenler eklemek için kullanılan anahtar-değer gösteriminde rota parametreleri. |
| Özel HTTP üstbilgileri         | İsteğe yerleştirilecek özel HTTP üstbilgileri. |
| HTTP isteği tanımlama bilgileri        | HTTP tanımlama bilgileri üstbilgi isteğine yerleştirilecek, anahtar-değer gösteriminde tanımlama bilgilerinin listesi. |
| Güvenlik protokolü           | Sunucuyla iletişim kurmak üzere HTTP istekleri için kullanılacak güvenlik protokolü. (Varsayılan olarak, Aktarım Katmanı Güvenliği \[TLS\] 1.2 kullanılıyor.) |

###### <a name="action-call-mexican-pac-service"></a>Eylem: Mexican PAC servisini çağır

| Parametre                | Tanım |
|--------------------------|-------------|
| Giriş dosyası               | Web hizmetine bir yöntem giriş parametresi olarak gönderilecek XML verilerini içeren dosya. |
| URL adresi              | Web hizmeti adresi (bitiş noktası). |
| Web yöntemi (eylem) adı | Çalıştırılması gereken Web yönteminin (eylem) adı. |
| Sertifikalar             | Web hizmeti tarafından istemci kimlik doğrulaması için gereken sertifika zinciri. İstemci sertifikası zincirdeki en son sertifika olmalıdır. Önce kök ve ara sertifikaların olması gerekir. |
| Web isteği zaman aşımı      | Web hizmeti yanıtı için beklenecek en uzun süre (milisaniye cinsinden). |
| Yeniden deneme aralığı           | Web hizmetinden bir yanıt alma girişimleri arasındaki zaman aralığı. Herhangi bir aralık belirtilmezse, ilk çağrı başarısız olduktan sonra ek denemeler yapılmaz. |
| Yeniden deneme sayısı              | Web hizmetinden gelen yanıtı çağırmaya ve almaya yönelik en fazla yeniden deneme girişimi sayısı. |
| Yeniden deneme süresi               | Yeniden deneme çağrısı devam etmeden önce beklenecek (milisaniye olarak) en fazla süre. |
| En az geri alma         | Yeniden deneme aralıklarının üssel hesaplanması için en az geri alma hızı. |
| En fazla geri alma         | Yeniden deneme aralıklarının üssel hesaplanması için en fazla geri alma hızı. |
| Güvenlik protokolü        | Sunucuyla iletişim kurmak üzere HTTP istekleri için kullanılacak güvenlik protokolü. (Varsayılan olarak TLS 1.2 kullanılır.) |

###### <a name="action-call-brazilian-sefaz-service"></a>Eylem: Brezilya SEFAZ hizmetini çağır

| Parametre                | Tanım |
|--------------------------|-------------|
| Giriş dosyası               | Web hizmetine bir yöntem giriş parametresi olarak gönderilecek XML verilerini içeren dosya. |
| URL adresi              | Web hizmeti adresi (bitiş noktası). |
| Web yöntemi (eylem) adı | Çalıştırılması gereken Web yönteminin (eylem) adı. |
| Sertifikalar             | Web hizmeti tarafından istemci kimlik doğrulaması için gereken sertifika zinciri. İstemci sertifikası zincirdeki en son sertifika olmalıdır. Önce kök ve ara sertifikaların olması gerekir. |
| Web isteği zaman aşımı      | Web hizmeti yanıtı için beklenecek en uzun süre (milisaniye cinsinden). |
| Yeniden deneme aralığı           | Web hizmetinden bir yanıt alma girişimleri arasındaki zaman aralığı. Herhangi bir aralık belirtilmezse, ilk çağrı başarısız olduktan sonra ek denemeler yapılmaz. |
| Yeniden deneme sayısı              | Web hizmetinden gelen yanıtı çağırmaya ve almaya yönelik en fazla yeniden deneme girişimi sayısı. |
| Yeniden deneme süresi               | Yeniden deneme çağrısı devam etmeden önce beklenecek (milisaniye olarak) en fazla süre. |
| En az geri alma         | Yeniden deneme aralıklarının üssel hesaplanması için en az geri alma hızı. |
| En fazla geri alma         | Yeniden deneme aralıklarının üssel hesaplanması için en fazla geri alma hızı. |
| Güvenlik protokolü        | Sunucuyla iletişim kurmak üzere HTTP istekleri için kullanılacak güvenlik protokolü. (Varsayılan olarak TLS 1.2 kullanılır.) |

###### <a name="action-call-italian-sdi-service"></a>Eylem: İtalya SDI Web servisini çağır

| Parametre                | Tanım |
|--------------------------|-------------|
| Giriş dosyası               | Web hizmetine bir yöntem giriş parametresi olarak gönderilecek XML verilerini içeren dosya. |
| URL adresi              | Web hizmeti adresi (bitiş noktası). |
| Web yöntemi (eylem) adı | Çalıştırılması gereken Web yönteminin (eylem) adı. |
| Sertifikalar             | Web hizmeti tarafından istemci kimlik doğrulaması için gereken sertifika zinciri. İstemci sertifikası zincirdeki en son sertifika olmalıdır. Önce kök ve ara sertifikaların olması gerekir. |
| Web isteği zaman aşımı      | Web hizmeti yanıtı için beklenecek en uzun süre (milisaniye cinsinden). |
| Yeniden deneme aralığı           | Web hizmetinden bir yanıt alma girişimleri arasındaki zaman aralığı. Herhangi bir aralık belirtilmezse, ilk çağrı başarısız olduktan sonra ek denemeler yapılmaz. |
| Yeniden deneme sayısı              | Web hizmetinden gelen yanıtı çağırmaya ve almaya yönelik en fazla yeniden deneme girişimi sayısı. |
| Yeniden deneme süresi               | Yeniden deneme çağrısı devam etmeden önce beklenecek (milisaniye olarak) en fazla süre. |
| En az geri alma         | Yeniden deneme aralıklarının üssel hesaplanması için en az geri alma hızı. |
| En fazla geri alma         | Yeniden deneme aralıklarının üssel hesaplanması için en fazla geri alma hızı. |
| Güvenlik protokolü        | Sunucuyla iletişim kurmak üzere HTTP istekleri için kullanılacak güvenlik protokolü. (Varsayılan olarak TLS 1.2 kullanılır.) |

### <a name="applicability-rules"></a>Uygulanabilirlik kuralları

Uygulanabilirlik kuralları, özellik kurulumu için kullanım bağlamını belirleyen mantıksal kurallar oluşturmanıza olanak sağlar. Böylece, işlem için gönderilen iş ile ilgili belge tarafından verilen bağlam ile uygulanabilirlik kuralı ölçütleriyle eşleşmesi söz konusu gönderimi işlemek için hangi elektronik faturalama eklentisi özelliğinin kullanılacağını belirler.

#### <a name="set-up-applicability-rules"></a>Uygulanabilirlik kurallarını kurma

1. **Özellik sürümü kurulumu** sayfasında, **Uygulanabilirlik kuralları** sekmesinde, uygulanabilirlik kuralı eklemek için **Yeni**'yi seçin.

    ![Uygulanabilirlik kurallarını yönetme](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. Kılavuzda, gruplandırılacak olan yan tümceleri seçin.
3. **Tümceyi gruplandır**'ı seçin.

    ![Tümceleri gruplama](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    Yan tümceler gruplandırıldığında, kılavuza yeni bir sütun eklenir. Bu sütun gruplanmış yan tümceler için mantıksal işleci belirtir.

    ![Gruplanmış yan tümceler için mantıksal işleç](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

Yan tümceleri çözmek için, grupları çözülecek gruplandırılmış tümceyi seçin ve sonra da **Yan tümce grubunu çöz** öğesini seçin.

![Yan tümcelerin grubunu çözme](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> Bir yan tümcenin grubunu çözdüğünüzde, her zaman en içteki gruplandırma düzeyinden başlayın.

Aşağıdaki tabloda, **Uygulanabilirlik kuralları** sekmesinde kullanılabilecek alanlar açıklanmaktadır.

| Alan         | Tanım |
|---------------|-------------|
| Ve/veya        | Mantıksal işleç. |
| Alan         | Kuralı oluşturmak için kullanılacak alan. |
| İşleç türü | İşleç türü:<ul><li>Eşittir</li><li>Eşit değil</li><li>Büyüktür/küçüktür</li><li>Büyük veya eşit / Küçük veya eşit</li><li>İçerir</li><li>Şununla başla</li></ul> |
| Değer         | Kural ölçütü. |

### <a name="variables"></a>Değişkenler

Değişkenler oluşturabilir ve belirli bir eylemin parametresi için giriş değeri olarak kullanabilirsiniz. Bunları, Elektronik faturalama eklenti hizmetleri ve istemci arasında, gönderim akışının kapsamında belirli bir eylemi yürütmenin sonucu olan bilgiler ile alış veriş yapmak için kullanabilirsiniz.

#### <a name="set-up-variables"></a>Değişkenlerini ayarla

- Değişkenleri yönetmek için, **Özellik sürümü kurulumu** sayfasında **Değişkenler** sekmesinde **Yeni**'yi veya **Sil**'i seçin.

    ![Değişkenleri yönetme](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

Aşağıdaki tabloda, **Değişkenler** sekmesinde kullanılabilecek alanlar açıklanmaktadır.

| Alan       | Tanım |
|-------------|-------------|
| Dosya Adı        | Değişkenin adı. |
| Tanım | Değişkenin kısa bir açıklaması. |
| Türü        | Değişken türü:<ul><li><strong>Sabit </strong>: Değişken içeriği sabittir.</li><li><strong>İstemciden </strong>: Microsoft Dynamics 365 istemcisinden gönderme işleminin yürütülmesi sırasında değişkenin içeriği alınır.</li><li><strong>İstemciye</strong>: Değişken içeriği Microsoft Dynamics 365 istemcisi tarafından içe aktarılabilmesi için hazır hale getirilir.</li></ul> |
| Veri türü   | Değişkenin veri tipi:<ul><li>Boole</li><li>Date</li><li>Sayı</li><li>UUID</li><li>Dize</li><li>Dosya</li></ul> |
| Değer       | Değişkenin değerini ayarlayan eylemin değeri veya değişkenin adı. |

### <a name="validate-the-feature-setup"></a>Özellik kurulumunu doğrulama

- **Özellik sürümü kurulumu** sayfasında, Eylem bölmesinde, özellik sürümü kurulumunu doğrulamak için **Doğrula**'yı seçin.

   ![Doğrula düğmesini seçme](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

Doğrulama tüm yapılandırmalarda tutarlılığını denetler. Örneğin, bir eylem için belirli bir parametre zorunlu ise ancak değeri boş kalırsa, doğrulama bu tutarsızlığı algılar ve bir uyarı verilir.

## <a name="environments"></a>Ortamlar

Elektronik faturalama eklenti ortamı, elektronik faturalama eklentisi özelliğiyle ilişkilendirilmiş ve bu özellik için etkinleştirilmiş olmalıdır. Elektronik faturalama eklenti ortamları, kuruluşunuzun RCS hesabındaki Genelleştirme özelliklerinin yapılandırılmasıyla önceden oluşturulup yayımlanmalıdır.

Elektronik faturalama eklenti ortamını, Elektronik faturalama eklentisi özelliği için etkinleştirmek üzere şu adımları izleyin.

1. Elektronik faturalama eklentisi ortamını eklemek için, **Elektronik faturalama eklentisi özellikleri** sayfasında **Ortamlar** sekmesinde **Etkinleştir**'i seçin.
2. **Geçerlilik başlangıcı** alanına, yeni ortamın geçerli olacağı tarihi girin.

![Elektronik faturalama eklentisi ortamını etkinleştirme](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>Kuruluşlar

Elektronik faturalama eklentisi özelliği birden çok kuruluş arasında paylaşılabilir.

- Elektronik faturalama eklenti özelliklerini paylaşmak istediğiniz kuruluşu eklemek için, **Elektronik faturalama eklenti özelliği** sayfasında **Kuruluşlar** sekmesinde, **Paylaş**'ı seçin.

Elektronik faturalama eklentisi özelliğini kuruluşla paylaşmayı durdurmak için, **Paylaşımını kaldır**'ı seçin.

## <a name="versions"></a>Sürümler

Sürümler, durumunu yöneterek Elektronik faturalama eklenti özelliği kullanım ömrünün kontrol altına alınmasına yardım eder. Var olan bir elektronik faturalama eklentisi özelliğinin yeni sürümünü oluşturabilir veya Elektronik faturalama eklentisi özelliği için tüm yapılandırmalar tamamlandığında, özelliğin durumunu **Tamamlandı** olarak, sonrasında da **Yayımla** olarak değiştirebilirsiniz.

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-add-on-feature"></a>Var olan bir Elektronik faturalama eklenti özelliğinin yeni sürümünü oluşturma

1. **Elektronik faturalama eklentisi özellikleri** sayfasında soldaki kılavuzda Elektronik faturalama eklenti özelliğini seçin.
2. **Sürümler** sekmesinde, elektronik faturalama eklentisi özelliğinin yeni bir sürümünü eklemek için **Yeni**'yi seçin.

### <a name="change-the-status-of-the-electronic-invoicing-add-on-feature"></a>Elektronik faturalama eklentisi özelliğinin durumunu değiştirme

Elektronik faturalama eklenti özelliğinin yaşam döngüsünü yönetmek için aşağıdaki adımları izleyin.

1. **Elektronik faturalama eklentisi özellikleri** sayfasında soldaki kılavuzda Elektronik faturalama eklenti özelliğini seçin.
2. **Sürümler** sekmesinde **Durumu Değiştir**'i seçin ve sonra durumu **Taslak**'tan **Tamamlandı**'ya değiştirin.
3. Elektronik faturalama eklentisi özelliğini ve tüm bileşenlerini tamamlamak istediğinizi onaylamanız istenir. Eylemi onaylamak için **Evet**'i, iptal etmek için **Hayır**'ı seçin.

    > [!NOTE]
    > **Evet**'i seçtiğinizde, Elektronik faturalama eklentisi özelliğinin bileşenleri olan yapılandırma sürümlerinin durumu otomatik olarak **Taslak**'tan **Tamamlandı**'ya geçer.

4. **Durumu Değiştir**'i seçin ve sonra durumu **Taslak**'tan **Yayımla**'ya değiştirin.
5. Elektronik faturalama eklentisi özelliğini ve tüm bileşenlerini Genel depoya yayımlamak istediğinizi onaylamanız istenir. Eylemi onaylamak için **Evet**'i, iptal etmek için **Hayır**'ı seçin.

    > [!NOTE]
    > **Evet**'i seçtiğinizde, yapılandırma versiyonlarının durumu otomatik olarak **Tamamlandı**'dan **Paylaşılanlar** olarak değiştirilir.
