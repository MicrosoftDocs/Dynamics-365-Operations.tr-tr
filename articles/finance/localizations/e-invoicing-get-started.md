---
title: Elektronik faturalama eklentisini kullanmaya başlangıç
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
manager: AnnBe
ms.date: 02/22/2021
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
ms.openlocfilehash: 56227e031f8205836bcae9ce26006fc8091c2863
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592562"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Elektronik faturalama eklentisini kullanmaya başlangıç

[!include [banner](../includes/banner.md)]

Bu konu, Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir.

Aşağıdaki tabloda Elektronik faturalama özellikleri ve uygulanabilecekleri iş belgeleri listelenmektedir.

| Özellik adı                         | İş belgesi |
|--------------------------------------|-------------------|
| Avusturya elektronik faturaları (AT)    | <p>Satış faturası</p><p>Proje faturası</p> |
| Belçika elektronik faturası (BE)      | <p>Satış faturası</p><p>Proje faturası</p> |
| Brezilya NF-e (BR)                  | <p>Mali belge modeli 55</p><p>Düzeltme mektubu</p> |
| Brezilya NFS-e ABRASF Curitiba (BR) | Servis Mali belgesi |
| Danimarka elektronik faturası (DK)       | <p>Satış faturası</p><p>Proje faturası</p> |
| Mısır elektronik faturası (EG)     | <p>Satış faturası</p><p>Proje faturası</p> |
| Estonya elektronik faturası (EE)     | <p>Satış faturası</p><p>Proje faturası</p> |
| Finlandiya elektronik faturası (FI)       | <p>Satış faturası</p><p>Proje faturası</p> |
| Fransa elektronik faturası (FR)       | <p>Satış faturası</p><p>Proje faturası</p> |
| Alman elektronik faturası (DE)       | <p>Satış faturası</p><p>Proje faturası</p> |
| FatturaPA (IT)                       | <p>Satış faturası</p><p>Proje faturası</p> |
| Meksika CFDI Interfactura (MX)       | <p>Satış faturası</p><p>Sevk irsaliyesi</p><p>Stok transferi</p><p>Ödeme tamamlayıcısı</p> |
| Hollanda elektronik faturası (NL)        | <p>Satış faturası</p><p>Proje faturası</p> |
| Norveç elektronik faturası (NO)    | <p>Satış faturası</p><p>Proje faturası</p> |
| İspanya elektronik faturası (ES)      | <p>Satış faturası</p><p>Proje faturası</p> |
| PEPPEOL elektronik faturası            | <p>Satış faturası</p><p>Proje faturası</p> |

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki prosedürleri tamamlamadan önce, aşağıdaki önkoşulların yerine getirilmesi gerekir:

- Elektronik faturalama eklentisine gönderim yapabilmek için Regulatory Configuration Service (RCS) ve Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management ortamınızı yapılandırın.
- Bir hizmet ortamı oluşturun ve elektronik faturalama eklentisinde yayınlayın. Daha fazla bilgi için bkz. [Elektronik faturalama eklentisi hizmet yönetimini kullanmaya başlangıç](e-invoicing-get-started-service-administration.md).
- Bağlı bir uygulama oluşturun. Daha fazla bilgi için bkz. [Elektronik faturalama eklentisi hizmet yönetimini kullanmaya başlangıç](e-invoicing-get-started-service-administration.md).
- Kuruluşunuz için bir yapılandırma sağlayıcısı oluşturun. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcısı oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Microsoft yapılandırma sağlayıcısından Elektronik faturalama özelliğini içeri aktarma 

1. Regulatory Configuration Service (RCS) hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Özellikler** bölümünde, **Elektronik faturalama eklentisi** kutucuğunu seçin.
3. **İçeri aktar**'ı seçin ve sonra **Eşitle**'yi seçin.
4. **Yapılandırma sağlayıcısı** sütununu **Microsoft** terimini göre filtreleyin.
5. Bu konunun başındaki tablodan elektronik faturalama özelliğinin adını seçin ve sonra **İçeri Aktar**'ı seçin.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Kuruluş sağlayıcınız altında Elektronik faturalama özelliği oluşturma

1. RCS'de **Genelleştirme özelliği** çalışma alanının **Özellikler** bölümünde, **Elektronik faturalama eklentisi** kutucuğunu seçin.
2. **Ekle** > **Var olan özelliğe göre**'yi seçin ve **Ad** alanına Elektronik faturalama özelliğinin adını girin.
3. **Açıklama** alanına özellik için bir açıklama girin.
4. **Temel özellik alanında**, Microsoft yapılandırma sağlayıcısından içeri aktarılan Elektronik faturalama özelliğini seçin.
5. **Özellik oluştur**'u seçin.

## <a name="configure-the-electronic-invoicing-feature"></a>Elektronik faturalama özelliğini yapılandırma

Ülke/bölgeye bağlı olarak, Elektronik faturalama özelliği ek yapılandırma gerektirebilir. 

Belirli adımlar için ülke/bölgeniz için kullanılabilen "Başlarken" belgelerine bakın.

## <a name="configure-the-application-setup"></a>Uygulama kurulumunu yapılandırma

1. Oluşturduğunuz elektronik faturalama özelliğini seçin.
2. **Sürüm** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın.
3. **Kurulumlar** sekmesinde **Uygulama Kurulumu**'nu seçin.

    > [!NOTE]
    > Kuruluşunuzun **Etkin** yapılandırma sağlayıcısı olarak ayarlı olduğunu doğrulayın. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

4. **Özellik kurulumu**'nu seçin ve sonra **Bağlı uygulama**'yı seçin.
5. **Elektronik belge türleri** bölümünde **Ekle**'yi seçin.
6. Özelliğin desteklediği her iş belgesi için aşağıdaki tabloya göre bir **Tablo adı** değeri seçip girin.

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

7. Özelliğin desteklediği her iş belgesi için aşağıdaki tabloya göre bir **Bağlam** değeri seçip girin.

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

8. Özelliğin desteklediği her iş belgesi için aşağıdaki tabloya göre bir **İş belgesi eşleme** değeri seçin ve girin.

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

Ülke/bölgeye bağlı olarak, Elektronik faturalama özelliği ek yapılandırma gerektirebilir.

Belirli adımlar için ülke/bölgeniz için kullanılabilen "Başlarken" belgelerine bakın.

## <a name="deploy-the-electronic-invoicing-feature"></a>Elektronik faturalama özelliğini dağıtma

1. **Sürümler** sekmesinde, dağıtmak istediğiniz Elektronik faturalama özelliği sürümünü seçin.
2. **Durumu değiştir** \> **Tamamla**'yı seçin.
3. **Durumu değiştir** \> **Yayınla**'yı seçin.
4. **Dağıt**'ı seçin.
5. **Bağlı uygulamaya dağıt** seçeneğini **Evet** olarak ayarlayın.
6. **Uygulama bağla** sayfasında, Finance veya Supply Chain Management krulumunuzla ilişkili bağlantıyı seçin.
7. **Hizmet ortamına dağıt** seçeneğini **Evet** olarak ayarlayın.
8. **Hizmet ortamı** alanında, Elektronik faturalama özelliğini dağıtmak istediğiniz Elektronik faturalama eklentisi hizmet ortamını seçin.
9. **Başlangıç tarihi** alanında, Elektronik faturalama özelliğinin Elektronik faturalama eklentisinde etkili olması gereken tarihi seçin.
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

- [Elektronik faturalama eklentisine genel bakış](e-invoicing-service-overview.md)
- [Elektronik faturalama eklentisi hizmet yönetimini kullanmaya başlama](e-invoicing-get-started-service-administration.md)
- [Brezilya için Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-bra-get-started.md)
- [Meksika için Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-mex-get-started.md)
- [İtalya için Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-ita-get-started.md)
- [Mısır'da elektronik müşteri faturaları](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
