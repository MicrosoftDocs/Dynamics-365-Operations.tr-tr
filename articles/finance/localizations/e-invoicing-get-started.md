---
title: Elektronik faturalamayı kullanmaya başlama
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 65944c3b73d5cecc8c86087729bcf8d2354c8f20
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2021
ms.locfileid: "6340167"
---
# <a name="get-started-with-electronic-invoicing"></a>Elektronik faturalamayı kullanmaya başlama

[!include [banner](../includes/banner.md)]

Bu konu, Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir. Bu konu, Regulatory Configuration Services (RCS) ve Dynamics 365 Finance içindeki genel konfigürasyon adımlarında size kılavuzluk eder ve iş belgelerini göndermek ve işleme sonuçlarını gözden geçirmek için izlemeniz gereken adımları sağlar.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki prosedürleri tamamlamadan önce, aşağıdaki önkoşulların yerine getirilmesi gerekir:

- Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) ve Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management ortamınızı yapılandırın. Daha fazla bilgi için bkz. [Elektronik faturalama hizmet yönetimini kullanmaya başlama](e-invoicing-get-started-service-administration.md).
- Kuruluşunuz için bir yapılandırma sağlayıcısı oluşturun. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Microsoft yapılandırma sağlayıcısından Elektronik faturalama özelliğini içeri aktarma 

1. Regulatory Configuration Service (RCS) hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
3. **İçeri aktar**'ı seçin ve sonra **Eşitle**'yi seçin.
4. **Yapılandırma sağlayıcısı** sütununu **Microsoft** terimini göre filtreleyin.
5. Bu konunun başındaki tablodan elektronik faturalama özelliğinin adını seçin ve sonra **İçeri Aktar**'ı seçin.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Kuruluş sağlayıcınız altında Elektronik faturalama özelliği oluşturma

1. RCS'te **Genelleştirme özelliği** çalışma alanının **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
2. **Ekle** > **Var olan özelliğe göre**'yi seçin ve **Ad** alanına Elektronik faturalama özelliğinin adını girin.
3. **Açıklama** alanına özellik için bir açıklama girin.
4. **Temel özellik alanında**, Microsoft yapılandırma sağlayıcısından içeri aktarılan Elektronik faturalama özelliğini seçin.
5. **Özellik oluştur**'u seçin.

## <a name="country-specific-configuration-for-electronic-invoicing-feature"></a>Elektronik faturalama özelliği için ülkeye özel yapılandırma

Ülke/bölgeye bağlı olarak, Elektronik faturalama özelliği belirli bir yapılandırma gerektirebilir. 

Belirli adımlar için ülke/bölgeniz için kullanılabilen "Başlarken" belgelerine bakın.

## <a name="import-the-model-mapping-configurations-from-electronic-reporting"></a>Elektronik raporlama için model eşleme yapılandırmalarını içe aktarma

1. RCS'de, **Elektronik raporlama** çalışma alanını seçin.
2. **Microsoft** yapılandırma sağlayıcı listesinden **depolar**'ı seçin.
3. **Genel**'i seçin ve eylem bölmesinde **aç**'ı seçin.
4. Model eşleme yapılandırmalarını aşağıdaki özellik adına göre oluşturulan tabloya uygun şekilde içe aktarın.

| Özellik adı                         | Model eşleme yapılandırması |
|--------------------------------------|-----------------------------|
| Avusturya elektronik faturaları (AT)    | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |
| Belçika elektronik faturası (BE)      | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |
| Brezilya NF-e (BR)                  | <p>Müşteri faturası bağlam modeli</p><p>Mali belgeler</p><p>Yanıt iletisi modeli</p> |
| Brezilya NFS-e ABRASF Curitiba (BR) | <p>Müşteri faturası bağlam modeli</p><p>Mali belgeler</p><p>Yanıt iletisi modeli</p> |
| Danimarka elektronik faturası (DK)       | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |
| Mısır elektronik faturası (EG)     | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p><p>Yanıt iletisi modeli</p> |
| Estonya elektronik faturası (EE)     | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |
| Finlandiya elektronik faturası (FI)       | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |
| Fransa elektronik faturası (FR)       | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |
| Alman elektronik faturası (DE)       | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |
| FatturaPA (IT)                       | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |
| Meksika CFDI Interfactura (MX)       | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p><p>Yanıt iletisi modeli</p> |
| Hollanda elektronik faturası (NL)        | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |
| Norveç elektronik faturası (NO)    | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |
| İspanya elektronik faturası (ES)      | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |
| PEPPEOL elektronik faturası            | <p>Müşteri faturası bağlam modeli</p><p>Fatura modeli</p> |


## <a name="configure-the-application-setup"></a>Uygulama kurulumunu yapılandırma

1. Oluşturduğunuz elektronik faturalama özelliğini seçin.
2. **Kurulumlar** sekmesinde **Uygulama Kurulumu**'nu seçin.
3. **Uygulama bağla** alanında Finance veya Supply Chain Management krulumunuzla ilişkili bağlantıyı seçin.
4. **Elektronik belge türleri** bölümünde **Ekle**'yi seçin.
5. Aşağıdaki tabloya göre bir **tablo adı** değeri seçin ve girin.

    | Özellik adı                         | İş belgesi | Tablo adı |
    |--------------------------------------|-------------------|------------|
    | Avusturya elektronik faturaları (AT)    | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | Belçika elektronik faturası (BE)      | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | Brezilya NF-e (BR)                  | <p>Mali belge</p><p>Düzeltme mektubu</p> | Mali belge |
    | Brezilya NFS-e ABRASF Curitiba (BR) | Servis Mali belgesi | Mali belge |
    | Danimarka elektronik faturası (DK)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | Mısır elektronik faturası (EG)     | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | Estonya elektronik faturası (EE)     | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | Finlandiya elektronik faturası (FI)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | Fransa elektronik faturası (FR)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | Alman elektronik faturası (DE)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | FatturaPA (IT)                       | <p>Satış faturası</p><p>Proje faturası | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | Meksika CFDI Interfactura (MX)       | <p>Satış faturası</p><p>Sevk irsaliyesi</p><p>Stok transferi</p><p>Ödeme tamamlayıcısı</p> | Müşteri fatura günlüğü |
    | Hollanda elektronik faturası (NL)        | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | Norveç elektronik faturası (NO)    | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | İspanya elektronik faturası (ES)      | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |
    | PEPPEOL elektronik faturası            | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri fatura günlüğü</p><p>Proje faturası</p> |

7. Oluşturduğunuz her tablo adı için aşağıdaki tabloya göre bir bağlam değeri seçin ve girin.

    | Özellik adı                         | İş belgesi | Bağlam |
    |--------------------------------------|-------------------|---------|
    | Avusturya elektronik faturaları (AT)    | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | Belçika elektronik faturası (BE)      | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | Brezilya NF-e (BR)                  | <p>Mali belge</p><p>Düzeltme mektubu</p> | <p>Müşteri faturası bağlam modeli – Mali belge bağlamı</p><p>Müşteri faturası bağlam modeli – FD düzeltme mektubu bağlamı</p> |
    | Brezilya NFS-e ABRASF Curitiba (BR) | Servis Mali belgesi| Müşteri faturası bağlam modeli – Mali belge bağlamı |
    | Danimarka elektronik faturası (DK)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | Mısır elektronik faturası (EG)     | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | Estonya elektronik faturası (EE)     | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | Finlandiya elektronik faturası (FI)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | Fransa elektronik faturası (FR)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | Alman elektronik faturası (DE)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | FatturaPA (IT)                       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | Meksika CFDI Interfactura (MX)       | <p>Satış faturası</p><p>Sevk irsaliyesi</p><p>Stok transferi</p><p>Ödeme tamamlayıcısı</p> | Müşteri faturası bağlam modeli – Müşteri faturası bağlamı |
    | Hollanda elektronik faturası (NL)        | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | Norveç elektronik faturası (NO)    | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | İspanya elektronik faturası (ES)      | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |
    | PEPPEOL elektronik faturası            | <p>Satış faturası</p><p>Proje faturası</p> | <p>Müşteri faturası bağlam modeli – Müşteri faturası bağlamı</p><p>Müşteri faturası bağlam modeli – Proje faturası bağlamı</p> |

8. Her tablo adı ve bağlamı için aşağıdaki tabloya göre bir iş belgesi eşleme değeri seçip girin.

    | Özellik adı                         | İş belgesi | İş belgesi eşleme |
    |--------------------------------------|-------------------|---------------------------|
    | Avusturya elektronik faturaları (AT)    | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | Belçika elektronik faturası (BE)      | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | Brezilya NF-e (BR)                  | <p>Mali belge</p><p>Düzeltme mektubu</p> | <p>Mali belge eşlemesi – Mali belge eşlemesi</p><p>Mali belge eşlemesi – düzeltme mektubu eşlemesi</p> |
    | Brezilya NFS-e ABRASF Curitiba (BR) | Servis Mali belgesi | Mali belge eşlemesi – Mali belge eşlemesi |
    | Danimarka elektronik faturası (DK)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | Mısır elektronik faturası (EG)     | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | Estonya elektronik faturası (EE)     | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | Finlandiya elektronik faturası (FI)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | Fransa elektronik faturası (FR)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | Alman elektronik faturası (DE)       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | FatturaPA (IT)                       | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | Meksika CFDI Interfactura (MX)       | <p>Satış faturası</p><p>Sevk irsaliyesi</p><p>Stok transferi</p><p>Ödeme tamamlayıcısı</p> | Fatura modeli eşlemesi – Müşteri faturası |
    | Hollanda elektronik faturası (NL)        | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | Norveç elektronik faturası (NO)    | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | İspanya elektronik faturası (ES)      | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |
    | PEPPEOL elektronik faturası            | <p>Satış faturası</p><p>Proje faturası</p> | <p>Fatura modeli eşlemesi – Müşteri faturası</p><p>Fatura modeli eşlemesi – Proje faturası</p> |


## <a name="country-specific-configuration-of-application-setup"></a>Uygulama kurulumunun ülkeye özel yapılandırması

Ülke/bölgeye bağlı olarak, Uygulama kurulumu özelliği belirli bir yapılandırma gerektirebilir. 

Belirli adımlar için ülke/bölgeniz için kullanılabilen "Başlarken" belgelerine bakın.

## <a name="deploy-the-electronic-invoicing-feature-to-service-environment"></a>Elektronik faturalama özelliğini servis ortamına dağıtma

1. **Sürümler** sekmesinde, dağıtmak istediğiniz Elektronik faturalama özelliği sürümünü seçin.
2. **Durumu değiştir** \> **Tamamla**'yı seçin.
3. **Durumu değiştir** \> **Yayınla**'yı seçin.
4. **Dağıt**'ı seçin.
5. **Bağlı uygulamaya dağıt** seçeneğini **Hayır** olarak ayarlayın.
6. **Hizmet ortamına dağıt** seçeneğini **Evet** olarak ayarlayın.
7. **Hizmet ortamı** alanında, Elektronik faturalama özelliğini dağıtmak istediğiniz Elektronik faturalama hizmet ortamını seçin.
8. **Başlangıç tarihi** alanında, Elektronik faturalama özelliğinin Elektronik faturalamada etkili olması gereken tarihi seçin.
9. **Tamam**'ı seçin.

## <a name="deploy-the-electronic-invoicing-feature-to-connected-application"></a>Elektronik faturalama özelliğini Bağlı uygulamaya dağıtma

1. **Sürümler** sekmesinde, dağıtmak istediğiniz Elektronik faturalama özelliği sürümünü seçin.
4. **Dağıt**'ı seçin.
5. **Bağlı uygulamaya dağıt** seçeneğini **Evet** olarak ayarlayın.
6. **Uygulama bağla** alanında Finance veya Supply Chain Management krulumunuzla ilişkili bağlantıyı seçin.
7. **Hizmet ortamına dağıt** seçeneğini **Hayır** olarak ayarlayın.
10. **Tamam**'ı seçin.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Finance veya Supply Chain Management'ta Elektronik faturalama özelliğini açma

1. Finance veya Supply Chain Management'ta oturum açın ve doğru tüzel kişilikte olduğunuzu doğrulayın.
2. **Kuruluş yönetimi** \> **Kurulum** \> **Elektronik belge parametreleri** bölümüne gidin.
3. **Özellikler** sekmesinde, Finance veya Supply Chain Management için elektronik faturalama özelliğini etkinleştirmek üzere ülkeye/bölgeye özgü özelliği seçin. Aşağıdaki tabloda, belirli bir ülke/bölge için kullanılabilen elektronik faturalama özelliklerinin listesi sağlanmaktadır. 

    | Özellik adı                                          | Ülke/bölge  |
    |-------------------------------------------------------|-----------------|
    | Avusturya elektronik faturaları (AT)                     | Avusturya         |
    | Belçika elektronik faturası (BE)                       | Belçika         |
    | CFDI Meksika elektronik faturası (MX)                  | Meksika          |
    | Danimarka elektronik faturası (DK)                        | Danimarka         |
    | Hollanda elektronik faturası (NL)                         | Hollanda |
    | Mısır elektronik faturası (EG)                      | Mısır           |
    | Estonya elektronik faturası (EE)                      | Estonya         |
    | Finlandiya elektronik faturası (FI)                       | Finlandiya         |
    | Fransa elektronik faturası (FR)                        | Fransa          |
    | Alman elektronik faturası (DE)                        | Almanya         |
    | İtalyan elektronik faturası (IT)                       | İtalya           |
    | NF-e Federal - Brezilya elektronik faturası (BR)      | Brezilya          |
    | NFS-e - Brezilya'ya özgü hizmet (şehir) elektronik fatura   | Brezilya          |
    | Norveç elektronik faturası (NO)                     | Norveç          |
    | PEPPEOL elektronik faturası                             | Genel          |
    | İspanya elektronik faturası (ES)                       | İspanya           |

4. **Kaydet**'i seçin.

## <a name="issue-electronic-invoices"></a>Elektronik fatura kesme

1. **Kuruluş yönetimi** \> **Periyodik** \> **Elektronik belgeler** \> **Elektronik belgeleri gönder**'e gidin.
2. **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin.
3. Sorgu filtresine tablo adı eklemek için **Ekle**'yi seçin.
4. Faturaları içeren tabloyu seçin.

    > [!NOTE]
    > Tablo adı, bu konunun önceki bölümlerindeki [Uygulama kurulumunu yapılandırma](#configure-the-application-setup) alanındaki tabloda listelenmelidir.

5. Sorgulamak istediğiniz tablodan alan adını seçin.
6. Sorgulanacak ölçütler için tablo adını ve alan adını girin.
7. Sorguya daha fazla alan ve ölçüt eklemek için 5 ve 6. adımı tekrarlayın ve **Tamam**'ı seçin.
8. **Tamam**'ı seçin.

## <a name="view-submission-logs"></a>Gönderme günlüklerini görüntüleme

1. **Kuruluş yönetimi** \> **Periyodik** \> **Elektronik belgeler** \> **Elektronik belgeleri gönderme günlüğü**'ne gidin.
2. **Belge türü** alanında, faturaları içeren tabloyu seçin.

    > [!NOTE]
    > Tablo adı, bu konunun önceki bölümlerindeki [Uygulama kurulumunu yapılandırma](#configure-the-application-setup) alanındaki tabloda listelenmelidir.

3. Kılavuzda bir fatura seçin ve ardından **Sorgula** \> **Gönderim ayrıntıları**'nı seçin.


## <a name="related-topics"></a>İlgili konular

- [Elektronik faturalamaya genel bakış](e-invoicing-service-overview.md)
- [Elektronik faturalama hizmet yönetimini kullanmaya başlama](e-invoicing-get-started-service-administration.md)
- [Brezilya için Elektronik faturalamayı kullanmaya başlama](e-invoicing-bra-get-started.md)
- [Meksika için Elektronik faturalamayı kullanmaya başlama](e-invoicing-mex-get-started.md)
- [İtalya için Elektronik faturalamayı kullanmaya başlama](e-invoicing-ita-get-started.md)
- [Mısır'da elektronik müşteri faturaları](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
