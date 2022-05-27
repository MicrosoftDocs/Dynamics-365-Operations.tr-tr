---
title: Vergi hesaplanmıyor veya vergi tutarı sıfır
description: Bu konu, vergi tutarı 0'sa (sıfır) veya vergi hesaplanmıyorsa yardımcı olabilecek sorun giderme bilgileri sağlar.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7237980f8d330a7b3f5c966d5bd3fff0eda8b21a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685870"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>Vergi hesaplanmıyor veya vergi tutarı sıfır

[!include [banner](../includes/banner.md)]

Bir harekette 0 (sıfır) olmayan bir satır tutarı olabilir ancak vergi hesaplanmıyordur veya hesaplanan vergi tutarı 0'dır. Bu sorunu gidermek için, aşağıdaki bölümlerde gereken adımları izleyin.

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>Vergi kodlarının hareket tarafından doğru şekilde seçildiğini doğrulayın

Hareket doğru vergi kodlarını seçmiyorsa veya hiçbir vergi kodu seçmiyorsa, bunlar üzerinde vergi hesaplanmaz. Vergi kodlarının hareket tarafından doğru şekilde seçildiğini doğrulamak için aşağıdaki adımları izleyin. 

1. Hareket satırında, **Satır ayrıntıları** hızlı sekmesinde, **Kurulum** sekmesinde, **Satış vergisi** bölümünde, **Madde satış vergisi grubu** ve **Satış vergisi grubu** alanlarında doğru vergi gruplarının seçilmiş olduğunu doğrulayın. Doğru vergi grupları seçilmemişse doğruları seçin.

    [![Madde satış vergisi grubu ve Satış vergisi grupları.](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. **Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi grupları**'na gidin.
3. Uygun satış vergisi grubunu seçin ve **Kurulum** hızlı sekmesinde **Satış vergisi kodu** alanındaki vergi kodunu not edin.

    [![Satış vergisi grupları sayfası.](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. **Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Madde satış vergisi grupları**'na gidin.
5. Uygun madde satış vergisi grubunu seçin ve **Kurulum** hızlı sekmesinde **Satış vergisi kodu** alanındaki vergi kodunun, satış vergisi grubunun vergi koduyla eşleştiğini doğrulayın.

    [![Madde satış vergisi grupları sayfası.](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. Vergi kodları eşleşmiyorsa gruplardan birinin satış vergisi kodunu güncelleştirin.

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>Seçilen vergi kodlarının muaf olmadığını ve doğru vergi oranı değerine sahip olduklarını doğrulayın

Vergi kodları muafsa veya vergi oranı 0 (sıfır) ise, vergi hesaplama sonucu 0 olur. Seçili vergi kodlarının muaf olup olmadığını ve bunlara doğru vergi oranının uygulanıp uygulanmadığını doğrulamak için aşağıdaki adımları izleyin.

1. **Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi grupları**'na gidin.
2. Uygun satış vergisi grubunu seçin ve **Kurulum** hızlı sekmesinde **Muafiyet** onay kutusunun işaretlenmemiş olduğundan emin olun. Onay kutusu işaretliyse işareti kaldırın.

    [![Satış vergisi grupları sayfasındaki Muafiyet onay kutusu.](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. **Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi kodları**'na gidin.
4. Uygun satış vergisi kodunu seçin ve **Değer** alanında vergi oranı değerinin 0 (sıfır) olmadığını doğrulayın. 0 ise, alanı doğru vergi oranına ayarlanmış şekilde güncelleştirin.

    [![Satış vergisi kod değerleri sayfasındaki değer alanı.](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>Doğru vergi tutarının sıfır olup olmadığını belirleyin

Bazı senaryolarda, vergi tutarı 0 (sıfır) doğrudur. Hareketiniz için 0'ın doğru vergi tutarı olup olmadığını belirlemek için aşağıdaki adımları izleyin.

1. **Genel muhasebe** \> **Genel muhasebe ayarı** \> **Genel muhasebe parametreleri**'ne gidin.
2. **Satış vergisi** sekmesinde, **Hesaplama yöntemi** alanında, **Toplam**'ın seçildiğini doğrulayın.

    [![Genel muhasebe parametreleri sayfasındaki Hesaplama yöntemi alanı.](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. **Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi kodları**'na gidin.
4. Uygun satış vergisi kodunu seçin, **Hesaplama** \> **Marjinal taban**'ı seçin ve marjinal tabanın, **Fatura bakiyesinin net tutarı** veya **Diğer satış vergi tutarları dahil fatura toplamı** olarak ayarlandığını doğrulayın. Daha fazla bilgi için bkz. [Diğer satış vergisi tutarları dahil fatura toplamı](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).
5. 2 ve 4 numaralı adımlarda doğru değerler ayarlıysa, hareketin toplam tutarının 0 (sıfır) olup olmadığını belirleyin. Toplam tutar 0 ise, vergi tutarının 0 olması beklenen sonuçtur. Vergi hesaplaması, fatura bakiyesinin toplam tutarını temel aldığından ve bu tutar satır başına olmadığından, vergi hesaplamasından sonraki her satıra 0 numaralı vergi tutarı tahsis edilir.

## <a name="determine-whether-customization-exists"></a>Özelleştirme olup olmadığını belirleyin

Önceki bölümlerdeki adımları tamamladıysanız ve bir sorun bulamadıysanız bir özelleştirme olup olmadığını belirleyin. Hiçbir özelleştirme yoksa daha fazla destek için bir Microsoft servis talebi oluşturun.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
