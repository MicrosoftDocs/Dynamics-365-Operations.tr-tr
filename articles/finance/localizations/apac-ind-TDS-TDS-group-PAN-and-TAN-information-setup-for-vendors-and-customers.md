---
title: Satıcılar ve müşteriler için TDS grubu, PAN ve TAN bilgilerini ayarlama
description: Bu konu, satıcı ve müşteriler için Kaynakta Kesilen Vergi (TDS) grubu, kalıcı hesap numarası (PAN) ve vergi hesap numarası (TAN) hakkında bilgilerin nasıl ayarlanacağını açıklamaktadır.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 808fa7b72651ab274415e48f5e0a356784ca6525
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407548"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>Satıcılar ve müşteriler için TDS grubu, PAN ve TAN bilgilerini ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, satıcı ve müşteriler için Kaynakta Kesilen Vergi (TDS) grubu, kalıcı hesap numarası (PAN) ve vergi hesap numarası (TAN) hakkında bilgilerin nasıl ayarlanacağını açıklamaktadır.

1. **Borç hesapları \> Satıcılar \> Tüm satıcılar** veya **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.

    [![Tüm satıcılar sayfası.](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. Eylem bölmesinde, satıcı veya müşteri oluşturmak üzere **Yeni**'yi seçin ve gerekli ayrıntıları girin. Alternatif olarak, varolan bir satıcı veya müşteriyi de seçebilirsiniz.
3. **Fatura ve teslimat** hızlı sekmesinde, **Stopaj vergisi** bölümünde, satıcı veya müşteri için stopaj vergisi, TDS veya Kaynakta Tahsil Edilen Vergiyi (TCS) hesaplamak için **Stopaj vergisini hesapla** seçeneğini **Evet** olarak ayarlayın.
4. Satınalma faturasının TDS'si, satıcı veya müşteri için tanımlanan varsayılan TDS grubu temel alınarak hesaplanır. **TDS grubu** alanında varsayılan TDS grubunu seçin.

    > [!NOTE]
    > **TDS grubu** alanında bir TDS grubunu seçtiğinizde, **Stopaj vergisi grubu** ve **TCS grubu** alanları kullanılamaz.

5. **Vergi bilgileri** hızlı sekmesinde, **PAN bilgileri** bölümünde, **Durum** alanında, satıcı veya müşteri için kalıcı hesap numarasının durumunu seçin:

    - **Mevcut değil** – Satıcı veya müşterinin bir PAN'ı yok.
    - **Alındı** – Satıcı veya müşterinin bir PAN'ı var.
    - **Başvurdu** – Satıcı veya müşteri, bir PAN için başvuruda bulunmuş.
    - **Geçersiz** – Satıcı veya müşterinin bir PAN'ı var ancak bu PAN geçerli değil.

6. Satıcının veya müşterinin bir PAN'ı olduğunu göstermek üzere **Durum** alanında **Alındı** seçeneğini belirlediyseniz PAN değerini **Numara** alanına girin. PAN beş alfabetik karakterden, dört sayısal karakterden ve ardından tek bir alfabetik karakterden oluşmalıdır. Aşağıda bir örnek verilmiştir: **ABCDE1260A**.
7. Satıcının veya müşterinin bir PAN için başvuruda bulunduğunu göstermek üzere **Durum** alanında **Başvurdu** seçeneğini belirlediyseniz referans numarasını **Referans numarası** alanına girin.
8. **Değerlendirilenin yapısı** alanında, satıcı veya müşterinin ait olduğu değerlendirilen yapısı kategorisini seçin:

    - Şirket
    - HUF
    - Kesinleştir
    - Kişi
    - AOP
    - BOI
    - Yerel makam
    - Diğerleri

    [![Vergi bilgileri hızlı sekmesi.](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. Eylem Bölmesinde, **Satıcı** sekmesinde, **Kayıt** grubunda, **Adresleri yönet** sayfasını açmak için **Kayıt Kimlikleri**'ni seçin.
10. **Adresleri yönet** sayfasında, **Vergi bilgileri** hızlı sekmesinde, vergi kayıt girişlerini yönetebildiğiniz **Vergi bilgilerini yönet** sayfasını açmak için **Ekle** veya **Düzenle**'yi seçin.
11. **Vergi bilgilerini yönet** sayfasında, **Stopaj vergisi** hızlı sekmesinde, **Vergi Hesap Numarası (TAN)** alanında, TAN'ı girin. TAN dört alfabetik karakterden, beş sayısal karakterden ve ardından tek bir alfabetik karakterden oluşmalıdır. Aşağıda bir örnek verilmiştir: **AFGH54821T**.
12. Sayfayı kapatın.
