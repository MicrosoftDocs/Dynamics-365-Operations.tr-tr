---
title: TDS yetkilisi ödemeleri için ödeme masraflarını ayarlama
description: Bu makalede, Kaynakta Kesilen Vergi (TDS) vergi dairesi ödemeleri için yapılan ödeme ücretlerinin nasıl ayarlanacağı açıklamaktadır.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 598d4c07d9f96fb5ae58c3929bab353a6d57615f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845233"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>TDS yetkilisi ödemeleri için ödeme masraflarını ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, Kaynakta Kesilen Vergi (TDS) vergi dairesi ödemeleri için yapılan ödeme ücretlerinin nasıl ayarlanacağı açıklamaktadır.

1. **Borç hesapları \> Ödeme kurulumu \> Ödeme masrafı**'na gidin.

    [![Ödeme ücreti sayfası.](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Ödeme ücreti oluşturmak için **Yeni**'yi seçin ve gerekli ayrıntıları girin.
3. **Ücret tipi** alanında ödeme ücreti türünü seçin:

    - **Hiçbiri**
    - **Faiz** – Faiz, TDS yetkili satıcısına yapılan geç ödemeler üzerinde ücretlendirildir.
    - **Diğer** – Diğer ücretler, TDS yetkili satıcısına yapılan geç ödemeler üzerinde ücretlendirildir.

    **Faiz** veya **Diğer**'i seçerseniz, **Ücret** alanı otomatik olarak **Genel muhasebe** olarak ayarlanır.

4. **Alan türü** alanında **Faiz** veya **Diğer**'i seçtiyseniz, **Ana hesap** alanında faiz veya diğer ücretlerin nakledileceği genel muhasebe hesabını seçin.
5. Gerekli diğer ayrıntıları girin.
6. Çeşitli bankalar, ödeme yöntemleri, ödeme özellikleri, para birimleri ve tarih aralıkları birleşimleri için ödeme ücretlerini ayarlayabileceğiniz **Ödeme ücreti kurulumu** sayfasını açmak için Eylem Bölmesinde, **Ödeme ücreti kurulumu**'nu seçin.

    [![Ödeme ücreti kurulumu sayfası.](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. **Genel bakış** sekmesinde, **Gruplandırmalar** alanında, ödeme ücretini hangi bankalar için ayarladığınızı belirtin:

    - **Tablo** – Ücret, belirli bir banka hesabı için geçerlidir.
    - **Grup** – Ücret, belirli bir banka grubu için geçerlidir.
    - **Tümü** – Ücret, tüm banka hesapları için geçerlidir.

8. **Gruplandırmalar** alanında **Tablo** veya **Grup**'u seçtiyseniz, **Banka ilişkisi** alanında, ödeme ücretini ayarladığınız belirli banka hesabını veya banka grubunu seçin.
9. **Ödeme yöntemi** alanında, ödeme ücretlerinin ödenmesi için ödeme yöntemini seçin.
10. **Ödeme özellikleri** alanında, **Ödeme özellikleri** sayfasında oluşturulan ödeme özelliği kodunu seçin veya girin.
    - Ödeme belirtimi, elektronik fon transferli ödeme yöntemleriyle birlikte kullanılır.
12. **Ödeme para birimi** alanında ücreti etkinleştiren para birimini seçin. Yalnızca seçilen para birimini kullanan hareketler ücreti etkinleştirebilir. Bu alanı boş bırakırsanız, tüm para birimleri ücreti etkinleştirir.
13. **Yüzde/Tutar** alanında, hesaplama yöntemini seçin. Seçenekler şöyledir: **Tutar**, **Yüzde** ve **Aralık**.
14. **Ücret tutarı** alanında, ödeme yüzdesi olarak veya bir ödemenin tutarı olarak ücret tutarını belirtin.
15. **Ücret para birimi** alanında ücretin para birimi kodunu belirtin.
16. Seçili banka hesabının ayrıntılarını görüntülemek veya değiştirmek için **Genel** sekmesini seçin.

    [![Genel sekmesi.](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. **Minimum** alanında, ücreti etkinleştirecek minimum hareket tutarını girin.
17. **Maksimum** alanında, ücreti etkinleştirecek maksimum hareket tutarını girin.
18. **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında, ücretleri hesaplamak için kullanılacak bir tarih aralığı tanımlayın.
19. **Minimum ücret** alanında, ödeme yüzdesi olarak veya bir ödemenin tutarı olarak ücret tutarını belirtin.
20. **Satış vergisi grubu** alanında, ücret tutarı için satış vergisini hesaplamak üzere kullanılacak satış vergisi grubunu seçin.
21. **Madde satış vergisi grubu** alanında, ücret tutarı için madde satış vergisini hesaplamak üzere kullanılacak madde satış vergisi grubunu seçin.
22. **Aralık** sekmesini seçin. 

    [![Aralık sekmesi.](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. **Günler** alanında, ödemenin nakil tarihi (iskonto tarihi) ve senedin vade tarihi arasındaki gün sayısını girin.
24. **Yüzde/Tutar** alanında, özelliğin yüzde mi yoksa belirli bir tutar mı olduğunu seçin.
25. **Ücret tutarı** alanında, ödeme yüzdesi olarak veya bir ödemenin tutarı olarak ücret tutarını girin.
26. **Ödeme ücreti kurulumu** sayfasını kapatın.
27. **Ödeme ücreti** sayfasını kapatın.
