---
title: Regulatory Configuration Services'teki (RCS) elektronik faturalamayı yapılandırma
description: Bu konuda, Dynamics 365 Regulatory Configuration Services'te (RCS) Elektronik faturalamanın nasıl yapılandırılacağı açıklanmaktadır.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 9958091db4a3d7ce0b625e5adc8e2a6b37878618
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840256"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a>Regulatory Configuration Services'teki (RCS) elektronik faturalamayı yapılandırma

[!include [banner](../includes/banner.md)]

Bu konu, Dynamics 365 Regulatory Configuration Services'teki (RCS) Elektronik faturalamanın yapılandırma yetenekleri hakkında bilgi sağlar.

Elektronik faturalamanın, herhangi bir kodlama yapmak zorunda kalmadan elektronik faturaların iş ve mevzuat gereksinimlerini karşılamanıza yardımcı olması yapılandırma özellikleri sayesindedir. Elektronik faturaların bir web hizmetleri tarafından elektronik olarak onaylanması gereken senaryolarda, yapılandırma özellikleri, herhangi bir kod yapmadan bir web hizmetleriyle ileti alışverişi gereksinimlerini karşılamanıza da yardımcı olur.

## <a name="electronic-reporting"></a>Elektronik raporlama

Elektronik raporlama (ER), Elektronik faturalamayı destekler.

Veri modeli eşlemesi ve biçimleri, ER aracılığıyla oluşturulan ve sürdürülen ve Elektronik faturalamada kullanılan yapılandırılabilir bileşenlerdir. ER biçimi tasarımcısı, dosya biçimleri oluşturmak ve bunları korumak için kullanılan bir araçtır. Elektronik faturalama özelliklerini yapılandırmak için kullanılır.

Daha fazla bilgi için bkz. [Elektronik raporlamaya (ER) genel bakış](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

## <a name="electronic-invoicing-features"></a>Elektronik faturalama özellikleri

Elektronik faturalama özellikleri, Elektronik faturalama aracılığıyla elektronik fatura oluşturmayı sağlar. Yapılandırma kurallarını kapsüllerler ve bunları Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'ın elektronik faturalama ve elektronik faturalara gönderdiği verileri işlemek için kullanırlar.

Özellikler ayrıca dosya biçimi teknik özelliklerine uygunluğun gerekli olduğu ve çıktının bağımsız bir elektronik dosya olduğu senaryoları da destekler. Çoğu durumda, dosya biçimi teknik özellikleri vergi dairesi tarafından yayınlanır.

Son olarak, özellikler, vergi dairesi veya bazı onaylı kuruluşlar taraflardan barındırılan harici web hizmetleriyle ileti alışverişini ve elektronik faturada yetkilendirme veya onay damgası taleplerini desteklemektedir.

### <a name="availability-of-electronic-invoicing-features"></a>Elektronik faturalama özelliklerinin kullanılabilirliği

Elektronik faturalama özelliklerinin kullanılabilirliği ülkeye veya bölgeye bağlıdır. Bazı özellikler genel kullanıma sunulsa da, diğerleri önizleme aşamasındadır.

#### <a name="preview-features"></a>Önizleme özellikleri

Aşağıdaki tabloda, şu anda önizleme aşamasında olan elektronik faturalama özellikleri gösterilmektedir.

| Ülke/bölge | Özellik adı                         | İş belgesi |
|----------------|--------------------------------------|-------------------|
| Avusturya        | Avusturya elektronik faturaları (AT)    | Satış faturaları ve proje faturaları |
| Belçika        | Belçika elektronik faturası (BE)      | Satış faturaları ve proje faturaları |
| Brezilya         | Brezilya NF-e (BR)                  | Mali belge modeli 55, düzeltme mektupları, iptaller ve atmalar |
| Brezilya         | Brezilya NFS-e ABRASF Curitiba (BR) | Hizmet mali belgeleri |
| Danimarka        | Danimarka elektronik faturası (DK)       | Satış faturaları ve proje faturaları |
| Mısır          | Mısır elektronik faturası (EG) | Satış faturaları ve proje faturaları |
| Estonya        | Estonya elektronik faturası (EE)     | Satış faturaları ve proje faturaları |
| Finlandiya        | Finlandiya elektronik faturası (FI)      | Satış faturaları ve proje faturaları |
| Fransa         | Fransa elektronik faturası (FR)       | Satış faturaları ve proje faturaları |
| Almanya        | Alman elektronik faturası (DE)       | Satış faturaları ve proje faturaları |
| İtalya          | FatturaPA (IT)                       | Satış faturaları ve proje faturaları |
| Meksika         | Meksika CFDI (MX)                    | Satış faturaları, sevk irsaliyeleri, stok transferleri, ödeme tamamlayıcıları ve iptaller |
| Hollanda    | Hollanda elektronik faturası (NL)        | Satış faturaları ve proje faturaları |
| Norveç         | Norveç elektronik faturası (NO)    | Satış faturaları ve proje faturaları |
| İspanya          | İspanya elektronik faturası (ES)      | Satış faturaları ve proje faturaları |
| Avrupa         | PEPPEOL elektronik faturası            | PEPPOL satış faturaları ve proje faturaları |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Elektronik faturalama özelliklerinin yapılandırılabilir bileşenleri

Elektronik faturalama özellikleri aşağıdaki yapılandırılabilir bileşen gruplarından oluşur:

- **Biçimler**: Biçimler, elektronik bir belge elektronik fatura haline geldiğinde Elektronik faturalamanın oluşturması gerekenleri yapılandırmanıza olanak tanır. Biçimler, elektronik fatura ve harici bir web hizmetiyle iletişim gerektiğinde istek göndermek ve yanıt almak için kullanılan dosyalar ve iletiler için biçim yapılandırmasını içerir.
- **Eylemler**: Eylemler, Elektronik faturalamanın Finance ve Supply Chain Management'ın elektronik faturaya gönderdiği elektronik belgenin dönüşümünü nasıl oluşturduğunu yapılandırmanıza olanak tanır.
- **Uygulanabilirlik kuralları**: Uygulanabilirlik kuralları, elektronik faturalama özelliğini işlemek için Elektronik faturalamanın göz önünde bulundurması gereken bağlamı yapılandırmanıza olanak tanır.
- **Değişkenler**: Değişkenler, yapılandırma mantığının yapısı için desteği yapılandırmanıza olanak tanır. Değişkenler, belirli bir eylemi gerçekleştirmek için değer girişleri olarak çalışabilir. Alternatif olarak, Finance ve Supply Chain Management ile Elektronik faturalama arasında bir değer takası olarak çalışabilirler.
- **Elektronik belge modeli eşlemesi**: Elektronik belge modeli eşlemesi, ER modeli eşlemesini yapılandırmanızı sağlar. Model eşleme, elektronik belgeler gönderildiğinde Elektronik faturalamaya entegre edilmiş soyut faturanın veri eşlemesini tanımlar.
- **Fatura bağlam modeli**: Fatura bağlam modeli, ER fatura bağlam modelini yapılandırmanıza ve elektronik faturalama özelliğinin bağlamını tanımlamanıza olanak tanır.
- **Yanıt türleri**: Yanıt türleri, elektronik fatura işlemenin bir sonucu olarak Elektronik faturalamanın Finance ve Supply Chain Management'ta güncelleştirilmesi gerekenleri yapılandırmanıza olanak tanır.

### <a name="formats"></a>Biçimler

Aşağıdaki listelerde, elektronik faturalama özellikleri için kullanılabilen ER biçimi yapılandırmaları gösterilmektedir.

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>Avusturya (AT) elektronik faturaları: Avusturya için satış ve proje faturaları

- OIOUBL Satış faturası
- OIOUBL Proje faturası
- OIOUBL Satış alacak dekontu
- OIOUBL Proje alacak dekontu

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>Belçika (BE) elektronik faturası: Belçika için satış ve proje faturaları

- UBL Satış faturası (BE)
- UBL Proje faturası (BE)
- UBL Proje alacak dekontu BE
- UBL Satış alacak dekontu BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>Brezilya (BR) NF-e: NF-e Federal (Brezilya)

- NF-e gönderim dışarı aktarma biçimi (BR)
- NF-e düzeltme mektubu dışarı aktarma biçimi (BR)
- NF-e iptal dışarı aktarma biçimi (BR)
- NF-e atma dışarı aktarma biçimi (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>Brezilya NFS-e (BR): NFS-e ABRASF Curitiba şehri

- NFS-e ABRASF Curitiba (BR)
- NFS-e ABRASF Sorgusu Curitiba (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>Danca (DK) elektronik fatura: Danimarka için satış ve proje faturaları

- OIOUBL Satış faturası
- OIOUBL Proje faturası
- OIOUBL Satış alacak dekontu
- OIOUBL Proje alacak dekontu

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>Felemenkçe (NL) elektronik fatura: Hollanda için satış ve proje faturaları

- UBL Satış faturası (NL)
- UBL Proje faturası (NL)
- UBL Proje alacak dekontu NL
- UBL Satış alacak dekontu NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>Mısır (EG) elektronik faturası: Mısır için satış ve proje faturaları

- Satış faturası (EG) (Faturalama)
- Proje faturası (EG) (Faturalama)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>Estonca (EE) elektronik fatura: Estonya için satış ve proje faturaları

- Satış faturası (EE)
- Proje faturası (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>Fince (FI) elektronik fatura: Finlandiya için satış ve proje faturaları

- Satış faturası (FI)
- Proje faturası (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>Fransızca (FR) elektronik fatura: Fransa için satış ve proje faturaları

- UBL Satış faturası (FR)
- UBL Proje faturası (FR)
- UBL Proje alacak dekontu FR
- UBL Satış alacak dekontu FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>Almanca (DE) elektronik fatura: Almanya için satış ve proje faturaları

- Satış faturası (DE)
- Proje faturası (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>İtalyanca (IT) elektronik fatura: İtalya için satış ve proje faturaları

- Satış faturası (IT)
- Proje faturası (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>Meksika (MX) CFDI: Meksika için CFDI

- CFDI fatura biçimi (MX)
- CFDI Sevk irsaliyesi (MX)
- CFDI Stok transferi (MX)
- CFDI ödeme biçimi (MX)
- CFDI fatura iptal biçimi (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>Norveççe (NO) elektronik fatura: Norveç için satış ve proje faturaları

- OIOUBL Satış faturası
- OIOUBL Proje faturası
- OIOUBL Satış alacak dekontu
- OIOUBL Proje alacak dekontu

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>PEPPOL elektronik faturası PEPPOL satış ve proje faturaları

- PEPPOL Satış faturası
- PEPPOL Proje faturası
- PEPPOL Satış alacak dekontu
- PEPPOL Proje alacak dekontu

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>İspanyolca (ES) elektronik fatura: İspanya için satış ve proje faturaları

- Satış faturası (ES)
- Proje faturası (ES)

### <a name="actions"></a>Eylemler

Aşağıdaki tabloda, kullanılabilir eylemler ve bunların şu anda genel kullanıma sunulup sunulmadığı veya hala önizleme aşamasında olup olmadığı listelenmektedir.

| Eylem                                        | Tanım                                                                  | Kullanılabilirlik         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Belgeyi dönüştür                            | Belgeyi dönüştürmek için Elektronik Raporlama biçimini çalıştırın.                   | Genel kullanılabilir  |
| XML belgesini imzalama                             | Xml belgelerini dijital imzayla imzalayın.                                   | Ön izlemede           |
| Mısır Vergi Dairesi için json belgesini imzalama | Mısır Vergi Dairesi için dijital imzalı json belgelerini imzalayın.       | Genel kullanılabilir  |
| Mısır ETA hizmeti ile tümleştirme           | Mısır Vergi Dairesi ile iletişim kurun.                                     | Genel kullanılabilir  |
| Brezilya SEFAZ Hizmetini çağırma                  | Mali belge gönderimi için Brezilya SEFAZ hizmeti ile tümleştirme yapın.       | Ön izlemede           |
| Meksika PAC Hizmetini çağırma                      | CFDI gönderimi için Meksika PAC hizmetiyle tümleştirme yapın.                      | Ön izlemede           |
| Yanıtı işle                              | Web hizmeti çağrısından alınan yanıtı analiz edin.                     | Genel kullanılabilir  |
| MS kullanma Power Automate                         | Microsoft Power Automate'te yerleşik akışla tümleştirme yapın.                       | Ön izlemede           |

## <a name="configuration-providers"></a>Konfigürasyon sağlayıcıları

Yapılandırma sağlayıcıları, elektronik faturalama özelliklerini ve model eşleme, biçim yapılandırması ve bağlam modeli gibi ER bileşenlerini sağlar. Elektronik faturalama özelliklerini ve ER bileşenlerini ilişkili Global depoda yayınlarlar. Oradan, diğer kuruluşlar bunları indirebilir.

Elektronik faturalama özelliklerini RCS aracılığıyla yapılandırmadan önce, **Elektronik raporlama** modülünde kendi kuruluşunuzu yapılandırma sağlayıcısı olarak yapılandırmanız gerekir. Yapılandırma sağlayıcısının **Etkin** olarak nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>Global depodaki elektronik faturalama özelliklerini görüntüleme

Belirli bir yapılandırma sağlayıcısının Global depoda bulunan elektronik faturalama özelliklerine göz atması için kuruluşunuzun RCS örneğini eşitleyin. Eşitleme tamamlandıktan sonra, kullanılabilir elektronik faturalama özelliklerinin listesi güncelleştirilir.

## <a name="importing-electronic-invoicing-features"></a>Elektronik faturalama özelliklerini içeri aktarma

Elektronik faturalama özelliklerini kullanmadan veya yapılandırmadan önce, bunları kuruluşunuzun RCS örneğine içeri aktarmalısınız. İçeri aktarma işlemi, özelliklerin yerel bir kopyasını oluşturur ve özelliklerin kullandığı tüm ER yapılarını (örneğin, biçim yapılandırmaları ve model yapılandırmaları) kuruluşunuzun RCS örneğine kopyalar.

Elektronik faturalama özelliklerini dilediğiniz yapılandırma sağlayıcısından alabilirsiniz.

## <a name="creating-electronic-invoicing-features"></a>Elektronik faturalama özellikleri oluşturma

Sıfırdan elektronik faturalama özelliği oluşturabilir veya başka bir elektronik faturalama özelliğinden özellik türetebilirsiniz.

Sıfırdan elektronik faturalama özelliği oluşturduğunuzda, ER bileşenlerini el ile eklemeniz gerekir (örneğin, özellik sürümü yapılandırmaları ve özellik sürümü kurulumu ve uygulama kurulumu gibi diğer yapılandırmalar). Bir özelliği başka bir özellikten türeterek oluşturduğunuzda, yeni özellik tüm yapılandırmaları orijinalinden devralır. 

## <a name="electronic-invoicing-feature-version"></a>Elektronik faturalama özelliği sürümü

Elektronik faturalama özelliklerinin sürümleri oluşturulur. Yeni bir sürüm oluşturulduğunda, sürüm numarası otomatik olarak artırılır. Yeni sürüm için "geçerlilik başlangıç" tarihi tanımlanabilir.

Elektronik faturalama özelliği sürümleri, en fazla üç durumu olan bir yaşam döngüsünü izler:

- **Taslak**: Bir özellik sürümü bu durumdaysa, yapılandırma özniteliklerini ve yapılarından herhangi birini (örneğin, dosya biçimi yapılandırmaları) düzenleyebilirsiniz.
- **Tamamlandı**: Bir özellik sürümü bu durumdaysa, kuruluşunuzla ilişkili Global depoda yayınlanmıştır. Artık özellik sürümünü veya ER bileşenlerinin hiçbirini düzenleyemezsiniz.
- **Yayınlandı**: Bir özellik sürümü bu durumdaysa, Elektronik faturalamada yayınlanmıştır. Artık özellik sürümünü veya ER bileşenlerinin hiçbirini düzenleyemezsiniz.

### <a name="feature-configurations"></a>Özellik yapılandırmaları

Özellik yapılandırmaları, elektronik faturalama özelliklerinin kullandığı tüm ER biçimi yapılandırmalarını tutar. Elektronik faturalama özelliğinin işleme sırasında kullandığı tüm elektronik dosyalar, bu özelliğin özellik yapılandırmalarına eklenen biçim yapılandırmalarından gelir.

Özellik yapılandırmalarından, biçim yapılandırmaları oluşturmak için kullanılan ER aracı olan ER biçim tasarımcısına erişebilirsiniz.

### <a name="feature-setup"></a>Özellik kurulumu

Özellik kurulumları, özellik yapılandırmalarıyla birlikte kullanılır. Her özellik kurulumu, elektronik faturalama özelliğinin elektronik faturanın belirli bir şartını karşılayabilmesi için beklenen davranışı sağlayan bir dizi eylemi, uygulanabilirlik kuralını ve değişkeni kapsüller.

### <a name="application-setup"></a>Uygulama kurulumu

Uygulama kurulumu daha önce oluşturulmuş bağlı bir uygulamayla ilişkilendirilmelidir.

Uygulama kurulumu üzerinden, Finance ve Supply Chain Management'ta yapılması gereken elektronik faturalama özelliğinin bir bölümünü yapılandırabilirsiniz. Elektronik faturalama özelliğinden bağımsız olarak en az üç yapılandırılabilir bileşen zorunludur:

- **Tablo adı**: Deftere nakledilen faturaları tutan ve elektronik faturalama özelliğinin temel aldığı Finance ve Supply Chain Management'taki varlık.
- **Bağlam**: ER üzerinden yapılandırılan fatura bağlam modelinin adı.
- **İş belgesi eşlemesi**: ER üzerinden yapılandırılan fatura eşleme modelinin adı.

> [!IMPORTANT]
> Uygulama kurulumuna girilen yapılandırma Finance ve Supply Chain Management'ta görüntülenebilir. **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametresi** bölümüne gidin. **Elektronik belge** sekmesinde, **Dağıt**'ı seçin ve ardından **Bağlı uygulama** seçeneğini belirleyin.

### <a name="deploying-feature-versions"></a>Özellik sürümlerini dağıtma

RCS'de, elektronik faturalama özelliği sürümünü hedef olarak yayınlamak için **Dağıt** komutunu kullanabilirsiniz. **Dağıt**'ı seçin ve sonra dağıtımın hedefini tanımlamak için aşağıdaki seçeneklerden birini belirleyin: 

- **Hizmet ortamı**: Dağıtımın hedefi hizmet ortamı olduğunda, elektronik faturalama özelliği sürümü hizmet ortamına yayınlanır. Elektronik faturalama daha sonra Finance ve Supply Chain Management'ın gönderdiği elektronik belgeleri almaya ve işlemeye hazır hale gelir.
- **Bağlı uygulama**: Dağıtımın hedefi bağlı uygulama olduğunda, uygulama kurulumu tarafından sağlanan yapılandırma, daha önce ilişkili olan Finance ve Supply Chain Management örneğine yazılır.

Yalnızca **Tamamlandı** durumuna sahip elektronik faturalama özelliği sürümleri bir hizmet ortamına veya bağlı bir uygulamaya dağıtılabilir.

### <a name="removing-feature-versions"></a>Özellik sürümlerini kaldırma

RCS'de, Elektronik faturalamadaki bir hizmet ortamından belirli bir elektronik faturalama özelliği sürümünü kaldırmak için **Dağıtımı kaldır** komutunu kullanabilirsiniz.

> [!IMPORTANT]
> **Dağıtımı kaldır** komutu yalnızca hizmet ortamlarında çalışır. Bağlı uygulamalardan elektronik faturalama özelliği sürümlerini kaldırmaz.

### <a name="rebasing-electronic-invoicing-features"></a>Elektronik faturalama özelliklerini yeniden temellendirme

Bir elektronik faturalama özelliği diğerinden türetildiğinde, **Yeniden Temelle** komutu, türetilen özelliği orijinal özellikte sunulan değişikliklerle güncelleştirir.

## <a name="additional-resources"></a>Ek kaynaklar

- [Finance ve Supply Chain Management'ta elektronik fatura kesme](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
