---
title: Vergi, fişte yanlış genel muhasebe hesabına naklediliyor
description: Bu konu, verginin fişteki yanlış genel muhasebe hesabına nakledilmesiyle ilgili sorun giderme bilgileri sağlar.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d60265df7ff1f447e20866b8b8a447d88db8cc4b3dccedebc0f18ce8f0f70dc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746332"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>Vergi, fişte yanlış genel muhasebe hesabına naklediliyor

[!include [banner](../includes/banner.md)]

Deftere nakledilme sırasında, vergi fişte yanlış genel muhasebe hesabına nakledilebilir. Bu sorunu gidermek için, aşağıdaki bölümlerde gereken adımları izleyin. Bu konudaki örneklerde, iş belgesi olarak bir satış siparişi kullanılır.

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>Yanlış nakledilen vergi hareketinin vergi kodunu bulma

1. **Fiş hareketleri** sayfasında, çalışmak istediğiniz hareketi seçin ve **Deftere nakledilen satış vergisi**'ni seçin.

    [![Fiş hareketleri sayfasındaki deftere nakledilen satış vergisi düğmesi.](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. **Satış vergisi kodu** alanındaki değeri inceleyin. Bu örnekte bu değer **VAT 19**'dur.

    [![Deftere nakledilen satış vergisi sayfasındaki satış vergisi kodu alanı.](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>Vergi kodunun genel muhasebe deftere nakil grubunu denetleme

1. **Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi kodları**'na gidin.
2. Vergi kodunu bulun ve seçin, sonra **Genel muhasebe deftere nakil grubu** alanındaki değeri gözden geçirin. Bu örnekte bu değer **VAT**'dır.

    [![Satış vergisi kodları sayfasındaki genel muhasebe deftere nakil alanı.](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. **Genel muhasebe deftere nakil grubu** alanındaki değer bir bağlantıdır. Grup yapılandırmasının ayrıntılarını görüntülemek için bağlantıyı seçin. Alternatif olarak, alanı seçin ve basılı tutun (veya sağ tıklayın) ve sonra **Ayrıntıları görüntüle**'yi seçin.

    [![Ayrıntıları görüntüle komutu.](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. **Satış vergisi borcu** alanında, hareket türüne göre hesap numarasının doğru olduğundan emin olun. Doğru değilse, deftere nakledilecek hesabı seçin. Bu örnekte, satış siparişinin satış vergisi, satış vergisi borçları hesabı 222200'e nakledilmelidir.

    [![Genel muhasebe deftere nakil grupları sayfasındaki satış vergisi borcu alanı.](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    Aşağıdaki tablo, **Genel muhasebe deftere nakil grupları** sayfasındaki her alan hakkında bilgi sağlar.

    | Alan                  | Tanım |
    |------------------------|-------------|
    | Satış vergisi borcu      | Vergi dairesine borç olan giden satış vergileri için ana hesap. |
    | Satış vergisi alacağı   | Vergi dairesinden alacak gelen vergiler için ana hesap. |
    | Kullanım vergisi gideri        | Avrupa Birliği (AB) ters gider Ürün ve Hizmet Vergisi (GST)/Uyumlaştırılmış Satış Vergisinin (HST) bir parçası olarak satıcıların talep etmediği ya da bildirmediği, vergiden düşülebilir kullanım vergilerini deftere nakledilmek için kullanılan ana hesap. Harekette kullanılan satış vergisi grubunda satış vergisi kodu için **Kullanım vergisi** seçeneği belirtilmelidir. **Genel muhasebe parametreleri** sayfasında **Satış vergisi vergilendirme kurallarını uygula** seçeneği belirtildiyse bu alan kullanılamaz. |
    | Kullanım vergisi borcu        | Vergi dairelerine ödenecek gelen kullanım vergilerini deftere nakletmek için kullanılan ana hesap. |
    | Kapatma hesabı     | **Kullanım vergisi borcu** ve **Satış vergisi alacağı** alanlarında belirtilen genel muhasebe hesaplarının net bakiyesinin nakledildiği ana hesap. |
    | Satıcı nakit iskontosu   | Bu genel muhasebe deftere nakil grubuyla ilişkili satış vergisi kodları için nakit iskontosunun nakledildiği ana hesap. |
    | Müşteri servis talebi iskontosu | Bu genel muhasebe deftere nakil grubuyla ilişkili satış vergisi kodları için nakit iskontosunun nakledildiği ana hesap. |

    Daha fazla bilgi için bkz. [Satış vergisi için Genel muhasebe deftere nakil grupları ayarlama](tasks/set-up-ledger-posting-groups-sales-tax.md).

## <a name="debug-in-code-to-check-ledger-dimensions"></a>Genel muhasebe boyutlarını denetlemek için kodda hata ayıklama

Kodda, deftere nakil hesabı genel muhasebe boyutuna göre belirlenir. Genel muhasebe boyutu, bir hesabın veritabanındaki kayıt kodunu kaydeder.

1. Bir satış siparişi için, bir **Tax::saveAndPost()** ve **Tax::post()** yöntemlerinde bir kesme noktası ekleyin. **\_ledgerDimension** değerine dikkat edin.

    [![Kesme noktası olan satış siparişi kodu örneği.](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    Bir satınalma siparişi için, **TaxPost::saveAndPost()** ve **TaxPost::postToTaxTrans()** yöntemlerinde bir kesme noktası ekleyin. **\_ledgerDimension** değerine dikkat edin.

    [![Kesme noktası olan satınalma siparişi kodu örneği.](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. Genel muhasebe boyutu tarafından kaydedilen kayıt koduna göre veritabanındaki hesabın görüntüleme değerini bulmak için aşağıdaki SQL sorgusunu çalıştırın.

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![Kayıt kodunun görünüm değeri.](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. **_ledgerDimension** değerinin nerede atandığını bulmak için çağrı yığınını inceleyin. Genellikle bu değer **TmpTaxWorkTrans**'tan alınır. Bu durumda, değerin atanma yerini bulmak için **TmpTaxWorkTrans::insert()** ve **TmpTaxWorkTrans::update()** yönteminde bir kesme noktası eklemeniz gerekir.

## <a name="determine-whether-customization-exists"></a>Özelleştirme olup olmadığını belirleyin

Önceki bölümlerdeki adımları tamamladıysanız ve bir sorun bulamadıysanız bir özelleştirme olup olmadığını belirleyin. Hiçbir özelleştirme yoksa daha fazla destek için bir Microsoft servis talebi oluşturun.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
