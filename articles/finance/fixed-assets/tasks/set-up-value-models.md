---
title: Değer modelleri ayarlama
description: Bu yordam, yeni bir sabit kıymet defterini nasıl oluşturacağınızı ve bir sabit kıymet grubuyla nasıl ilişkilendireceğinizi gösterir.
author: moaamer
ms.date: 12/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be3b5578bd6509859c36f6a50ea9730e9ef1780e
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2021
ms.locfileid: "7890724"
---
# <a name="set-up-value-models"></a>Değer modelleri ayarlama

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Bu yordam, yeni bir sabit kıymet defterini nasıl oluşturacağınızı ve bir sabit kıymet grubuyla nasıl ilişkilendireceğinizi gösterir.

## <a name="create-a-book"></a>Defter oluşturma
1. **Sabit kıymetler \> Kurulum \> Defterler**'e gidin.
2. **Yeni**'yi seçin.
3. **Defter** alanına bir değer girin.
4. **Açıklama** alanında bir değer girin.
5. **Amortismanı hesapla** seçeneğini **Evet** olarak ayarlayın.

    **Amortismanı hesapla** seçeneği **Evet** olarak ayarlanırsa ilgili kıymet defteri amortisman tekliflerine dahil edilir. **Hayır** olarak ayarlanırsa kıymet defteri otomatik olarak amortismana tabi edilmez.

6. **Amortisman profili** alanına bir değer girin veya seçin.

    * Alternatif bir amortisman profili de aynı zamanda amortisman geçiş yöntemi olarak bilinir. Alternatif profil, varsayılan amortisman profilininkine eşit veya ondan büyük bir amortisman tutarı hesaplarsa, amortisman teklifi bu profile geçer.
    * Olağandışı durumlarda bir kıymetin ek amortismanı için Olağandışı amortisman profili kullanılır. Örneğin bunu doğal felaketlerden kaynaklanan amortismanı kaydetmek için kullanabilirsiniz.
    * **Temel düzeltmeler bulunan amortisman düzeltmeleri oluştur**'u seçerseniz kıymetin değeri güncelleştirildiği zaman otomatik olarak amortisman düzeltmeleri oluşturulur. Aksi takdirde, güncelleştirilmiş kıymet değeri yalnızca gelecekteki amortisman hesaplamalarını etkiler.

7. **Temel ayarlamalarla amortisman ayarlamaları oluştur** seçeneğini **Evet** olarak ayarlayın.

    * Varsayılan olarak, sabit kıymet defteri hareketlerini genel muhasebeye nakleder. Ancak defter için **Genel muhasebeye naklet** işlemini, Genel muhasebeye naklet seçeneğini **Hayır** olarak ayarlayarak devre dışı bırakabilirsiniz. Genel muhasebeye nakledilmeyen defterler genellikle vergi raporlama amacıyla kullanılır. Bu seçenek, hareketler genel muhasebeye işlenmediğinden kıymet defterine ait geçmiş hareketleri silmek için ek esneklik sağlar.
    * Varsayılan olarak, **Deftere nakil katmanı** alanı, defter genel muhasebeye nakledilirse **Geçerli katman**, ve genel muhasebeye nakledilmezse **Hiçbiri** olarak ayarlanır. Bu defterin hareketlerinin farklı bir katmana nakledilmesi gerekiyorsa **Deftere nakil katmanı** alanının değerini güncelleştirin.

8. Pozitif amortismanı hesaplayın.

    * Varsayılan olarak, **Artı amortismanı hesapla** seçeneği **Hayır** olarak ayarlanır. Bu ayar, amortismanın seçili kıymet defterini alacaklandıracağını gösterir. Ayrıca, **Edinme fiyatından daha yüksek net defter değerine izin ver** ve **Negatif net defter değerine izin ver** seçeneklerinin her ikisi de **Hayır** olarak ayarlanır ve ayarlar bağımsız olarak değiştirilebilir. 
    * Pozitif amortismanı hesaplamak için **Pozitif amortismanı hesapla** seçeneğini **Evet** olarak ayarlayın. Bu ayar, amortismanın sabit kıymet defterini borçlandıracağını gösterir. **Pozitif amortisman hesapla** seçeneği **Evet** olarak ayarlandığında, **Edinme fiyatından yüksek net defter değerine izin ver** ve **Negatif net defter değerine izin ver** seçenekleri otomatik olarak **Evet** olarak ayarlanır ve kilitlenir. Bu kilit, pozitif amortismanın yalnızca negatif defter değeri (alacak) ile alınan sabit kıymetlere uygulanmasına yardımcı olur. 

10. **Takvim** alanına bir değer girin veya buradan bir değer seçin.

    Türetilmiş defterler hareketleri aynı anda farklı defterlere nakleder. Hareketleri birincil defter ile oluşturursunuz ve deftere nakletme sırasında hareketin tam bir kopyası türev defterine nakledilir. Türev defteri hareketleriyle yeniden hesaplama olmaz, bu nedenle amortisman hareketlerinde kullanılmamalıdır.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Defteri bir sabit kıymet grubuyla ilişkilendirin

1. **Sabit kıymet grupları**'nı seçin.
2. **Sabit kıymet grubu** alanında bir değer girin veya seçin.
3. **Servis ömrü** alanına bir sayı girin.

    * Amortisman dönemleri, sabit kıymetin servis ömrü girildikten sonra hesaplanır.
    * Amortisman yöntemi, vergi amacıyla gerektiği şekilde ayarlanabilir.
    * Kiralamalarla ilişkili sabit kıymetler için **Hizmet ömrü** alanının değeri, kıymet defterindeki kiralama süresinin daha azı ve kıymetin kullanım ömrü tarafından geçersiz kılınır. Kiralama defteri için **Sahiplik aktarımı** seçeneği **Evet** olarak ayarlanırsa **Hizmet ömrü** alanının değeri her zaman kıymetin kullanım ömrü olacaktır.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
