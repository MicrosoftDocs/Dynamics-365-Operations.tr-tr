---
title: Elektronik faturalama eklentisini yönetim bileşenleri
description: Bu konu, elektronik faturalama eklentisinin yönetimiyle ilgili bileşenler hakkında bilgi sağlar.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104450"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>Elektronik faturalama eklentisini yönetim bileşenleri

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Bu konu, elektronik faturalama eklentisinin yönetimiyle ilgili bileşenler hakkında bilgi sağlar. Elektronik faturalama eklentisi hizmetinin nasıl yapılandırılacağı hakkında bilgiler de sağlar.

## <a name="azure"></a>Azure

Anahtar kasası ve depolama hesabının gizli dizilerini oluşturmak için Microsoft Azure kullanın. Sonra, Elektronik faturalama eklentisinin yapılandırmasında gizli dizileri kullanın.

## <a name="lifecycle-services"></a>Lifecycle Services

LCS dağıtım projenizde mikro hizmetler için eklentiyi etkinleştirmek amacıyla Microsoft Dynamics Lifecycle Services'i (LCS) kullanın.

LCS'de, **Önizleme özelliği yönetimi** kutucuğunu seçin ve sonra **E-faturalama hizmeti** özelliğini etkinleştirin.

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS), elektronik faturalama eklentisini konfigüre etmek için kullanılan arabirimdir. Ortamlar ve elektronik faturalama özellikleri gibi kaynaklar RCS'de oluşturulur, sürdürülür ve barındırılır. Kaynaklar hazır olduğunda, elektronik faturalama eklentisi hizmetine yayınlanırlar.

RCS hakkında daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).

### <a name="integration-with-the-electronic-invoicing-add-on"></a>Elektronik faturalama eklentisi ile tümleştirme

Elektronik faturaları konfigüre etmek için RCS'yi kullanabilmeniz için önce, RCS'yi Elektronik faturalama eklentisi ile iletişime izin verecek şekilde konfigüre etmelisiniz. Bu konfigürasyon **Elektronik raporlama parametreleri** sayfasındaki **Elektronik faturalama eklentisi** sekmesinde tamamlanmalıdır.

#### <a name="service-endpoint"></a>Hizmet bitiş noktası

Elektronik faturalama eklentisi uç noktasının URL'si, Azure veri merkezi coğrafyasına göre değişebilir. Aşağıdaki tabloda her bölge için kullanılabilirlik listelenmiştir:

| Azure veri merkezi coğrafyası | Hizmet uç noktası URL'si                                                       |
|----------------------------|----------------------------------------------------------------------------|
| Doğu ABD                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| Batı ABD                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| Kuzey AB                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| Batı AB                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a>Başvuru kodu

Uygulama kimliği, Elektronik faturalama eklenti uygulamasının kimliğidir. Bu durumda değer sabittir: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

#### <a name="lcs-environment-id"></a>LCS ortam kimliği

LCS ortamı kimliği, kuruluşunuzun LCS aboneliğinin kimliğidir.

### <a name="service-environments"></a>Hizmet ortamları

Hizmet ortamları, Elektronik faturalama eklentisinin elektronik faturalama özelliklerinin yürütülmesini desteklemek için oluşturulan mantıksal bölümlerdir. Güvenlik gizli dizileri ve dijital sertifikalar ve idare (erişim izinleri), hizmet ortamı düzeyinde konfigüre edilmelidir.

Müşteriler istedikleri sayıda servis ortamı oluşturabilir. Bir müşterinin oluşturduğu tüm servis ortamları birbirinden bağımsızdır.

Hizmet ortamları, RCS'de oluşturulup tutulmalıdır. Hizmet ortamları hazır olduğunda, elektronik faturalama eklentisi hizmetine yayınlanmalıdır.

#### <a name="service-environment-status"></a>Hizmet ortamı durumu

Hizmet ortamları, durum ile yönetilebilir. Olası seçenekler şunlardır:

- **Yayınlanmadı** – Ortam oluşturuldu, ancak henüz yayınlanmadı.
- **Yayınlandı** – Ortam elektronik faturalama eklentisi içinde yayınlanmıştır.
- **Değiştirildi** – Yayınlanmış bir ortamın öznitelikleri değiştirildi, ancak değişiklikler henüz yayınlanmadı.

#### <a name="customer-secrets"></a>Müşteri gizli dizileri

Elektronik faturalama eklentisi servisi, tüm iş verilerinizi şirketinize ait Azure kaynaklarında depolamaktan sorumlu olur. Hizmetin doğru çalışmasını ve elektronik faturalama eklentisi için gerekli olan ve bu eklenti tarafından oluşturulan ve yalnızca eklenti tarafından oluşturulmuş tüm iş verilerine erişmesini sağlamak için iki ana Azure kaynağı oluşturmanız gerekir:

- Elektronik faturaları depolayacak bir Azure depolama hesabı (Blob depolama)
- Sertifikaları ve depolama hesabının Tekdüzen Kaynak Tanımlayıcısı'nı (URI) depolamak için bir Azure Key Vault

> [!NOTE]
> Özel bir Anahtar Kasası kaynağı ve müşteri depolama hesabıyla özel olarak Elektronik faturalama eklentisi ile kullanılmak üzere ayrılmalıdır.

Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).

#### <a name="users"></a>Kullanıcılar

Her bir hizmet ortamı, elektronik faturalama eklentilerinde Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'tan bağlanabilecek kullanıcıları listelemelidir.

#### <a name="publication"></a>Yayınlama

Hizmet ortamlarının kullanılması için elektronik faturalama eklentisi hizmetine yayınlanmalıdır. Finance ve Supply Chain Management tarafından yalnızca yayınlanan ortamlara erişilebilir. Ek olarak, hizmet ortamının özniteliklerinde yapılacak güncelleştirmeler elektronik faturalama servisi üzerinde geçerli olmadan önce hizmet ortamı yayınlanmalıdır.

### <a name="connected-applications"></a>Bağlı uygulamalar

Bağlı uygulamalar, RCS üzerinden erişmek isteyebileceğiniz Finance ve Supply Chain Management kurulumlarıdır. Uygulama URL'si ve kiracısının yanı sıra bağlı bir uygulama, RCS'nin ortama bağlanmasına olanak veren kimlik bilgilerini içerir.

Bağlı uygulamalar sayesinde, Finance ve Supply Chain Management'ta elektronik faturalama özelliğinin bir kısmını, tüm elektronik faturalama özelliğini çalışır hale getirmek için konfigüre edebilirsiniz.

## <a name="finance-and-supply-chain-management"></a>Finance ve Supply Chain Management

### <a name="integration-with-electronic-invoicing-add-on"></a>Elektronik faturalama eklentisi ile tümleştirme

Elektronik faturalama eklentisi üzerinden elektronik faturalar kesmek amacıyla Finance ve Supply Chain Management'ı kullanabilmeniz için eklentinin hizmetle iletişim kurulmasına izin verecek şekilde konfigüre edilmesi gerekir.

#### <a name="electronic-invoicing-add-on-integration-feature"></a>Elektronik faturalama eklentisi tümleştirme özelliği

Finance ve Supply Chain Management ile Elektronik faturalama eklentisi arasındaki iletişimi etkinleştirmek için **Özellik yönetimi** çalışma alanındaki **Elektronik faturalama eklentisi tümleştirme** özelliğini açmanız gerekir.

#### <a name="service-endpoint"></a>Hizmet bitiş noktası

Servis uç noktası, elektronik faturalama eklentisinin bulunduğu URL'dir. Elektronik fatura kesebilmek için Finance ve Supply Chain Management'ta servis uç noktalarının yapılandırılarak hizmetle iletişim kurulmasına izin vermesi gerekir.

Hizmet uç noktasını konfigüre etmek için **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametresi**'ne gidin ve **Gönderme hizmetleri** sekmesinde, **Elektronik faturalama eklentisi URL'si** alanına, **Servis uç noktası** bölümünde açıklanan şekilde tabloya URL'yi girin.

#### <a name="environments"></a>Ortamlar

Finance ve Supply Chain Management'a girilen ortam adı, RCS'de oluşturulan ve Elektronik faturalama eklentisine yayınlanan ortam adına başvurur.

Ortam, elektronik fatura kesmeye yönelik her isteğin, Elektronik faturalama eklentisinin hangi elektronik faturalama özelliğinin talebi işlemesi gerektiğini belirleyebildiği bir ortam içermesi için **Elektronik belge parametresi** sayfasının **Gönderim servisleri** sekmesinde konfigüre edilmelidir.

## <a name="additional-resources"></a>Ek kaynaklar

- [RCS'de elektronik faturaları yapılandırma](e-invoicing-configuration-rcs.md)
- [Finance ve Supply Chain Management'ta elektronik fatura kesme](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
