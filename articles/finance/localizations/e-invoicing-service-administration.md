---
title: Elektronik faturalama yönetim bileşenleri
description: Bu konu, elektronik faturalama yönetimiyle ilgili bileşenler hakkında bilgi sağlar.
author: gionoder
ms.date: 08/31/2021
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
ms.openlocfilehash: d187e8a03552258099d7021ff056d0726ea60ca1
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463893"
---
# <a name="electronic-invoicing-administration-components"></a>Elektronik faturalama yönetim bileşenleri

[!include [banner](../includes/banner.md)]


Bu konu, elektronik faturalama yönetimiyle ilgili bileşenler hakkında bilgi sağlar. Elektronik faturalama hizmetinin nasıl yapılandırılacağı hakkında bilgiler de sağlar.

## <a name="azure"></a>Azure

Anahtar kasası için gizli diziler oluşturmak ve depolama hesabı ayarlamak için Microsoft Azure kullanın. Ardından, Elektronik faturalama yapılandırmasında anahtar kasası gizli dizilerini ve depolama hesabı SAS belirtecini kullanın.

## <a name="lifecycle-services"></a>Lifecycle Services

LCS dağıtım projeniz için Elektronik faturalama Eklentisini etkinleştirmek için Microsoft Dynamics'te Lifecycle Services'i (LCS) kullanın.

> [!NOTE]
> Eklentilerin LCS'ye yüklenmesi için en az bir **Katman 2 ortamı** gerekir. Ortam planlama hakkında daha fazla bilgi için [ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) konusuna bakın.
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS), elektronik faturalamayı yapılandırmak için kullanılan arabirimdir. Ortamlar ve elektronik faturalama özellikleri gibi kaynaklar RCS'de oluşturulur, sürdürülür ve barındırılır. Kaynaklar hazır olduğunda, elektronik faturalama hizmetine yayınlanırlar.

RCS kaydı için, bkz. [Regulatory services](https://marketing.configure.global.dynamics.com/).

RCS hakkında daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).

### <a name="integration-with-electronic-invoicing"></a>Elektronik faturalama ile tümleştirme 

Elektronik faturaları konfigüre etmek için RCS'yi kullanabilmeniz için önce, RCS'yi Elektronik faturalama ile iletişime izin verecek şekilde konfigüre etmelisiniz. Bu konfigürasyon **Elektronik raporlama parametreleri** sayfasındaki **Elektronik faturalama** sekmesinde tamamlanmalıdır.

#### <a name="service-endpoint"></a><a id='svc-endpoint-uris'></a>Hizmet bitiş noktası

Elektronik faturalama çeşitli Azure veri merkezi coğrafyalarında mevcuttur. Aşağıdaki tabloda her bölge için kullanılabilirlik listelenmiştir.


| Veri merkezi Azure coğrafyası | Hizmet uç noktası URI'si                                                       |
|----------------------------|----------------------------------------------------------------------------|
| Amerika Birleşik Devletleri              | <p>https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing</p> |
| Avrupa                     | <p>https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Birleşik Krallık             | <p>https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Asya                       | <p>https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |

### <a name="service-environments"></a>Hizmet ortamları

Hizmet ortamları, Elektronik faturalamada genelleştirme özelliklerinin yürütülmesini desteklemek için oluşturulan mantıksal bölümlerdir. Güvenlik gizli dizileri ve dijital sertifikalar ve idare (erişim izinleri), hizmet ortamı düzeyinde konfigüre edilmelidir.

Müşteriler istedikleri sayıda servis ortamı oluşturabilir. Bir müşterinin oluşturduğu tüm servis ortamları birbirinden bağımsızdır.

Hizmet ortamları, RCS'de oluşturulup tutulmalıdır. Hizmet ortamları hazır olduğunda, elektronik faturalama hizmetine yayınlanmalıdır.

#### <a name="service-environment-status"></a>Hizmet ortamı durumu

Hizmet ortamları, durum ile yönetilebilir. Olası seçenekler şunlardır:

- **Yayınlanmadı** – Ortam oluşturuldu, ancak henüz yayınlanmadı.
- **Yayınlandı** – Ortam elektronik faturalama içinde yayınlanmıştır.
- **Değiştirildi** – Yayınlanmış bir ortamın öznitelikleri değiştirildi, ancak değişiklikler henüz yayınlanmadı.

#### <a name="customer-secrets"></a>Müşteri gizli dizileri

Elektronik faturalama servisi, tüm iş verilerinizi şirketinize ait Azure kaynaklarında depolamaktan sorumlu olur. Hizmetin doğru çalışmasını ve elektronik faturalama eklentisi için gereken ve bu eklenti tarafından oluşturulan tüm iş verilerine düzgün biçimde erişildiğinden emin olmak için iki ana Azure kaynağı oluşturmanız gerekir:

- Elektronik faturalar, belge dönüştürmelerinin sonuçları ve harici web hizmetlerinden gelen yanıtlar dahil olmak üzere elektronik belgeleri depolayacak bir Azure depolama hesabıdır (Blob depolama).
- Sertifikaları ve depolama hesabının tekdüzen kaynak tanımlayıcısı'nı (URI) depolamak için bir Azure anahtar kasası (SAS token).


Özel bir Key Vault kaynağı ve müşteri depolama hesabıyla özel olarak Elektronik Faturalama ile kullanılmak üzere ayrılmalıdır. Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir Key Vault oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).

Key Vault'un sağlığını izlemek ve uyarı almak üzere, Key Vault için Azure İzleyici'yi yapılandırın. Key Vault günlüğünü etkinleştirerek, Key Vault'larınıza nasıl, ne zaman ve kim tarafından erişildiğini izleyebilirsiniz. Daha fazla bilgi için bkz. [Azure Key Vault için izleme ve uyarı](/azure/key-vault/general/alert) ve [Key Vault günlüğünü etkinleştirme](/azure/key-vault/general/howto-logging?tabs=azure-cli).

Bir en iyi uygulama olarak, gizli anahtarları düzenli olarak döndürün. Daha fazla bilgi için bkz. [Gizli anahtar belgeleri](/azure/key-vault/secrets/).

#### <a name="users"></a>Kullanıcılar

Her bir hizmet ortamı, elektronik faturalamalarda Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'tan bağlanabilecek kullanıcıları listelemelidir.

#### <a name="publication"></a>Yayınlama

Hizmet ortamlarının kullanılması için elektronik faturalama hizmetine yayınlanmalıdır. Finance ve Supply Chain Management tarafından yalnızca yayınlanan ortamlara erişilebilir. Ek olarak, hizmet ortamının özniteliklerinde yapılacak güncelleştirmeler elektronik faturalama servisi üzerinde geçerli olmadan önce hizmet ortamı yayınlanmalıdır.

### <a name="connected-applications"></a>Bağlı uygulamalar

Bağlı uygulamalar, RCS üzerinden erişmek isteyebileceğiniz Finance ve Supply Chain Management kurulumlarıdır. Uygulama URL'si ve kiracısının yanı sıra bağlı bir uygulama, RCS'nin ortama bağlanmasına olanak veren kimlik bilgilerini içerir.

Bağlı uygulamalar sayesinde, Finance ve Supply Chain Management'ta elektronik faturalama özelliğinin bir kısmını, tüm elektronik faturalama özelliğini çalışır hale getirmek için konfigüre edebilirsiniz.

## <a name="finance-and-supply-chain-management"></a>Finance ve Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>Elektronik faturalama ile tümleştirme

Elektronik faturalama üzerinden elektronik faturalar kesmek amacıyla Finance ve Supply Chain Management'ı kullanabilmeniz için hizmetle iletişim kurulmasına izin verecek şekilde konfigüre edilmesi gerekir.

#### <a name="electronic-invoicing-integration-feature"></a>Elektronik faturalama tümleştirme özelliği

Finance ve Supply Chain Management ile Elektronik faturalama arasındaki iletişimi etkinleştirmek için **Özellik yönetimi** çalışma alanındaki **Elektronik faturalama tümleştirme** özelliğini açmanız gerekir.

#### <a name="service-endpoint"></a>Hizmet bitiş noktası

Servis uç noktası, elektronik faturalamanın bulunduğu URL'dir. Elektronik fatura kesebilmek için Finance ve Supply Chain Management'ta servis uç noktalarının yapılandırılarak hizmetle iletişim kurulmasına izin vermesi gerekir.

Servis uç noktasını yapılandırmak için **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri**'ne gidin ve ardından **Elektronik faturalama** sekmesindeki **Uç nokta URL'si** alanında bu konunun önceki bölümlerinde yer alan [Hizmet bitiş noktası](#svc-endpoint-uris) bölümündeki tablodan uygun URL'yi girin.

#### <a name="environments"></a>Ortamlar

Finance ve Supply Chain Management'a girilen ortam adı, RCS'de oluşturulan ve Elektronik faturalamaya yayınlanan ortam adına başvurur.

Ortam, **Elektronik belge parametreleri** sayfasının **Elektronik faturalama** sekmesinde yapılandırılmalıdır. Bu şekilde, her elektronik fatura yayınlama isteği, Elektronik faturalamanın hangi elektronik faturalama özelliğinin isteği işlemesi gerektiğini belirleyebileceği ortamı içerir.

## <a name="additional-resources"></a>Ek kaynaklar

- [RCS'de elektronik faturaları yapılandırma](e-invoicing-configuration-rcs.md)
- [Finance ve Supply Chain Management'ta elektronik fatura kesme](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
