---
title: Elektronik faturalama yönetim bileşenleri
description: Bu konu, elektronik faturalama yönetimiyle ilgili bileşenler hakkında bilgi sağlar.
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
ms.openlocfilehash: 2e859875e124796e49000cd5ea94cfb75ecd768a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840040"
---
# <a name="electronic-invoicing-administration-components"></a>Elektronik faturalama yönetim bileşenleri

[!include [banner](../includes/banner.md)]


Bu konu, elektronik faturalama yönetimiyle ilgili bileşenler hakkında bilgi sağlar. Elektronik faturalama hizmetinin nasıl yapılandırılacağı hakkında bilgiler de sağlar.

## <a name="azure"></a>Azure

Anahtar kasası ve depolama hesabının gizli dizilerini oluşturmak için Microsoft Azure kullanın. Sonra, Elektronik faturalamanın yapılandırmasında gizli dizileri kullanın.

## <a name="lifecycle-services"></a>Lifecycle Services

LCS dağıtım projenizde mikro hizmetleri etkinleştirmek amacıyla Microsoft Dynamics Lifecycle Services'i (LCS) kullanın.

> [!NOTE]
> LCS içindeki mikro hizmetin yüklenmesi için en az bir katman 2 sanal makine gereklidir. Ortam planlama hakkında daha fazla bilgi için [ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) konusuna bakın.
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS), elektronik faturalamayı yapılandırmak için kullanılan arabirimdir. Ortamlar ve elektronik faturalama özellikleri gibi kaynaklar RCS'de oluşturulur, sürdürülür ve barındırılır. Kaynaklar hazır olduğunda, elektronik faturalama hizmetine yayınlanırlar.

RCS kaydı için, bkz. [Regulatory services](https://marketing.configure.global.dynamics.com/).

RCS hakkında daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).

### <a name="integration-with-electronic-invoicing"></a>Elektronik faturalama ile tümleştirme 

Elektronik faturaları konfigüre etmek için RCS'yi kullanabilmeniz için önce, RCS'yi Elektronik faturalama ile iletişime izin verecek şekilde konfigüre etmelisiniz. Bu konfigürasyon **Elektronik raporlama parametreleri** sayfasındaki **Elektronik faturalama** sekmesinde tamamlanmalıdır.

#### <a name="service-endpoint"></a>Hizmet bitiş noktası

Elektronik faturalama çeşitli Azure veri merkezi coğrafyalarında mevcuttur. Aşağıdaki tabloda her bölge için kullanılabilirlik listelenmiştir.

| Azure veri merkezi coğrafyası |
|----------------------------|
| Doğu ABD                    |
| Batı ABD                    |
| Kuzey AB                   |
| Batı AB                    |

### <a name="service-environments"></a>Hizmet ortamları

Hizmet ortamları, Elektronik faturalamanın elektronik faturalama özelliklerinin yürütülmesini desteklemek için oluşturulan mantıksal bölümlerdir. Güvenlik gizli dizileri ve dijital sertifikalar ve idare (erişim izinleri), hizmet ortamı düzeyinde konfigüre edilmelidir.

Müşteriler istedikleri sayıda servis ortamı oluşturabilir. Bir müşterinin oluşturduğu tüm servis ortamları birbirinden bağımsızdır.

Hizmet ortamları, RCS'de oluşturulup tutulmalıdır. Hizmet ortamları hazır olduğunda, elektronik faturalama hizmetine yayınlanmalıdır.

#### <a name="service-environment-status"></a>Hizmet ortamı durumu

Hizmet ortamları, durum ile yönetilebilir. Olası seçenekler şunlardır:

- **Yayınlanmadı** – Ortam oluşturuldu, ancak henüz yayınlanmadı.
- **Yayınlandı** – Ortam elektronik faturalama içinde yayınlanmıştır.
- **Değiştirildi** – Yayınlanmış bir ortamın öznitelikleri değiştirildi, ancak değişiklikler henüz yayınlanmadı.

#### <a name="customer-secrets"></a>Müşteri gizli dizileri

Elektronik faturalama servisi, tüm iş verilerinizi şirketinize ait Azure kaynaklarında depolamaktan sorumlu olur. Hizmetin doğru çalışmasını ve elektronik faturalama eklentisi için gereken ve bu eklenti tarafından oluşturulan tüm iş verilerine düzgün biçimde erişildiğinden emin olmak için iki ana Azure kaynağı oluşturmanız gerekir:

- Elektronik faturaları depolayacak bir Azure depolama hesabı (Blob depolama)
- Sertifikaları ve depolama hesabının Tekdüzen Kaynak Tanımlayıcısı'nı (URI) depolamak için bir Azure Key Vault

> [!NOTE]
> Özel bir Anahtar Kasası kaynağı ve müşteri depolama hesabıyla özel olarak Elektronik faturalama ile kullanılmak üzere ayrılmalıdır.

Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).

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

Hizmet uç noktasını konfigüre etmek için **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametresi**'ne gidin ve **Gönderme hizmetleri** sekmesinde, **Elektronik faturalama URL'si** alanına, **Servis uç noktası** bölümünde açıklanan şekilde tabloya URL'yi girin.

#### <a name="environments"></a>Ortamlar

Finance ve Supply Chain Management'a girilen ortam adı, RCS'de oluşturulan ve Elektronik faturalamaya yayınlanan ortam adına başvurur.

Ortam, elektronik fatura kesmeye yönelik her isteğin, Elektronik faturalamanın hangi elektronik faturalama özelliğinin talebi işlemesi gerektiğini belirleyebildiği bir ortam içermesi için **Elektronik belge parametresi** sayfasının **Gönderim servisleri** sekmesinde konfigüre edilmelidir.

## <a name="additional-resources"></a>Ek kaynaklar

- [RCS'de elektronik faturaları yapılandırma](e-invoicing-configuration-rcs.md)
- [Finance ve Supply Chain Management'ta elektronik fatura kesme](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
