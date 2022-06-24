---
title: Borç hesapları için fatura eşleştirme doğrulaması ayarlama
description: Bu makale, doğrulama ile ilgili borç hesapları fatura eşleştirmesinin nasıl ayarlanacağı konusunda bilgi sağlar.
author: abruer
ms.date: 02/14/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86cc5cf688e3b66cf976fc7f507bd8f8df757612
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904973"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Borç hesapları fatura eşleştirme doğrulaması ayarlama

[!include [banner](../../includes/banner.md)]

Başlamadan önce Fatura eşleştirme yapılandırma anahtarının seçildiğinden emin olun. Tüzel kişilik navlun vb. gibi masrafları giderleri kullanarak takip ediyorsa, Masraflar yapılandırma anahtarının seçili olduğundan emin olun.  Borç hesapları faturası eşleştirme, satıcı faturasını, satın alma siparişini ve ürün alındı bilgilerini eşleştirme işlemidir. Bu belgelerin aralarındaki farklara eşleştirme uyuşmazlıkları denir. Eşleştirme uyuşmazlıkları, belirtilen toleranslarla karşılaştırılır. Bir eşleştirme uyuşmazlığı tolerans yüzdesini veya tutarını aşarsa, **Satıcı faturası** sayfasında ve **Fatura eşleştirme ayrıntıları** sayfasında eşleşme farkı simgeleri görüntülenir.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Hangi faturanın hangi fatura ile eşleştirileceğini belirleme
Dört farklı eşleşen doğrulama türü vardır. 

- **Satır düzeyi eşleme** – En yaygın eşleşme türü satır eşleşmesidir. Satır düzeyi eşleştirme iki yönlü veya üç yönlü eşleştirme olabilir. **Borç hesapları parametresi** sayfasındaki yasal bir varlık için varsayılan satır düzeyi eşleştirme belirtilebilir. İki yollu eşleştirme faturadaki birim fiyatını satın alma siparişindeki birim birim fiyatıyla karşılaştırır. Üç yönlü eşleştirme ek olarak, fatura miktarını eşleşen ürün giriş miktarıyla karşılaştırır.
- **Fatura toplamları eşleştirmesi** – Satınalma siparişindeki toplam tutarları, fatura üzerindeki toplam tutarlara eşleştirin. Bu tür fatura eşleştirmesi fatura eşleştirme bilgileri gözden geçirmek ve denetimlerini ayarlamak için gerekli olan personel süresini en aza indirmek amacıyla bu seçeneği kullanabilmeniz için en az ayrıntı miktarını içerir. Alt toplam, alt toplamderl, toplam iskonto, Masraflar, Satış vergileri, Yuvarlama ve Fatura tutarı da dahil karşılaştırılır. Fatura üzerindeki bu değerlerin herhangi birinin kabul edilebilir bir varyansa göre beklenen tutarlardan sapması halinde sistem tarafından doğrulanır.
- **Gider eşleştirme** – Faturadaki gider bilgisini (tutarları) satınalma siparişi üzerindeki gider bilgisi (tutarlar) ile eşleştirir.
- **Satır maddesi eşleştirme için fiyat toplamları** – bu tip eşleştirme, genellikle tek bir satın alma siparişi satırı için birden fazla fatura alan şirketler için yararlıdır. Satınalma sipariş satırı başına genellikle yalnızca tek bir fatura alıyorsanız bu eşleştirme türü gerekli değildir. Bu eşleştirme, iki yönlü veya üç yönlü eşleştirmesinin etkinleştirilmesini gerektirir ve tolerans yüzdeleri ve tutarları temel alarak, aşılmamış bir net tutar doğrulaması işlevi görür.  Bu tür bir eşleşme faturadaki her bir satırın net tutarıyla ilgili fiyat bilgilerini ve tüm bekleyen ve önceden nakledilmiş fatura satırlarını, karşılık gelen satınalma siparişi satırının net tutarıyla karşılaştırır. Net tutar aşağıdaki formül kullanılarak belirlenir: (Birim fiyat * Satır miktarı) + Satır giderleri - Satır indirimleri. Fiyat toplamlarını yüzde ile eşleştirirken, sistem değerleri hareketin para birimini kullanarak karşılaştırır. Fiyat toplamlarını tutara göre eşleştirirken, sistem değerleri muhasebe para birimini kullanarak karşılaştırır.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>Parametreleri fatura eşleştimre doğrulaması ayarlama
1. **Borç hesapları > Kurulum > Borç hesapları parametreleri**'ne gidin.
2. **Fatura doğrulama** sekmesine tıklayın.
3. **Faturalama eşleştirme doğrulamayı** etkinleştirin onay kutusunu işaretleyin veya işareti kaldırın.
    * Fatura eşleşme uyuşmazlıkları bulunan bir faturanın deftere nakledilebilmesi için onay gerekip gerekmediğini belirtin. Bu ayar **Uyarıyla izin ver** yapıldıysa fatura eşleştirmedeki bir uyuşmazlık toleransı aştığı zaman görsel bir gösterge çıkar. Ancak yine de faturayı deftere nakledebilirsiniz. Fatura eşleştirme doğrulamasıyla birlikte iş akışları kullanmak istiyorsanız, bir kereden fazla onaylamak zorunda kalmamak için, **Uyuşmazlıkları olan faturayı deftere naklet** alanının **Uyarıyla izin ver** olarak ayarlandığından emin olun.  
    * **Fatura başlığı durumunu otomatik olarak güncelleştir** alanında, fatura veri girişi sırasında sistem tarafından otomatik eşleştirme yapılıp yapılmayacağını belirtin. Veri giriş performansında sorunlar yaşamadığınız sürece, önerilen ayar **Evet**'tir. Otomatik güncelleştirmeleri devre dışı bırakmak, fatura verileri girilirken fatura eşleştirme doğrulaması atlanacağı için daha hızlı sistem performansı sağlayabilir. Bu ayar **Hayır** yapılırsa veri giriş görevlisinin, fatura eşleştirme doğrulaması sonuçlarını görmek için fatura eşleştirme durumunu el ile güncelleştirmesi gerekir.  
4. **Fatura toplamları eşleştirme**'yi ayarlama.
5. Gerçek fatura toplamlarını beklenen toplamlarla eşleştirmek için, **Fatura toplamlarını eşleştir** onay kutusunu seçin veya kutunun işaretini kaldırın.
    * Fatura eşleştirmesindeki bir uyuşmazlık toleransı aştığı zaman simge görüntülenip görüntülenmeyeceğini belirtin. Toleransı aşan uyuşmazlık pozitif olduğunda veya pozitif ya da negatif olduğunda simge görüntülenmesini seçebilirsiniz.  
    * Örneğin, tolerans yüzde 5 ve satınalma siparişindeki toplam fatura tutarı 100,00 olsun. Bu nedenle, faturadaki toplam fatura tutarı 105,00'i aştığı takdirde bir fiyat eşleşme simgesi görüntülenir. **Büyükse veya düşükse toleransı**'nı seçerseniz, simge, fatura tutarının 95,00'ten az olması durumunda da görüntülenir.  
6. **Fatura toplamları tolerans yüzdesi** alanına kabul edilebilir yüzde farkını girin. Bu değer şirketin varsayılan değeridir. Bu değer, **Fatura Toplamları Toleransları** sayfası kullanılarak belirli satıcılar için geçersiz kılınabilir. Belirli bir satıcı için fatura toplamları tolerans yüzdesini geçersiz kılma hakkında bilgi için bu makalenin ilerleyen bölümlerindeki "Satıcılar için fatura toplamları eşleştirme toleransını ayarlama" bölümüne bakın.
7. **Fiyat ve miktar eşleştirme**'yi ayarlayın.
8. **Satır eşleştirme ilkesi** alanında birlikte çalıştığınız tüzel kişilik için varsayılan ilke olarak kullanılacak değeri seçin. **Gerekli değil**, tekil fatura satırı fiyatlarının satınalma siparişi fiyatıyla veya fatura miktarlarının sevk irsaliyesi miktarlarıyla eşleştirilmesinde doğrulama yapmak gerekmediği anlamına gelir. **İki Yönlü Eşleştirme** fatura satırlarının doğrulanması gerekmediği, ancak satınalma siparişi ve tedarikçi fatura belgelerinin doğrulamaya dahil edileceği anlamına gelir. Ürün girişi, eşleştirme doğrulamalarında dikkate alınmaz. **Üç Yönlü Eşleştirme** fatura net birim fiyatının satınalma siparişi net birim fiyatıyla karşılaştırılacağı ve eşleşen ürün girişi miktarının fatura miktarıyla karşılaştırılacağı anlamına gelir.
9. Bir madde, satıcı, satıcı ve madde birleşimi veya satınalma siparişi satırı için uygulanacak eşleştirmede farklı bir düzeye izin vermek için alanında **Eşleştirme ilkesini geçersiz kılmaya izin ver** alanında bir değer seçin. **Eşleştirme ilkesi** sayfasında belirli bir satıcı, madde veya satıcı ve madde birleşimi için tüzel kişilik satır Eşleştirme ilkesinin üzerine yazılabilir.
    * Satır eşleştirme ilkesi olarak İki yönlü eşleştirme veya Üç yönlü eşleştirme kullanıyorsanız, **Madde fiyat toleransı** sayfasında tüzel kişiliğiniz, maddeler ve satıcılar için fiyat toleransı yüzdeleri ayarlayabilirsiniz. Yasal varlık varsayılan fiyat toleransı, iki yönlü ve üç yönlü eşleştirme için sıfır olarak ayarlanır. Satıcı faturaları, satınalma siparişlerindeki bilgilerle karşılaştırılırken, ilgili fiyat toleransı yüzdesi aranır.   
10. Faturalardaki satır maddelerinin fiyat toplamlarını eşleştirmek için, **Fiyat toplamlarını eşleştir** alanında bir değer seçin. Satıcı aynı satınalma siparişi satırı için birden fazla fatura gönderdiği zaman bu eşleştirme türü yararlı olur. Faturadaki her bir satırın net tutarıyla ilgili fiyat bilgilerini ve tüm bekleyen ve önceden nakledilmiş fatura satırlarını, karşılık gelen satınalma siparişi satırının net tutarıyla karşılaştırabilirsiniz.  Seçenekler arasında **Hiçbiri**, **Yüzde**, **Tutar** veya **Yüzde ve tutar** bulunur.
11. **Satınalma fiyatı toplam tolerans yüzdesi** alanına, kabul ettiğiniz farkın yüzdesini girin. Bu alan yalnızca  **Fiyat toplamlarını eşleştir** alanında **Yüzde** veya **Yüzde ve tutar** değeri seçildiğinde kullanılabilir
12. **Satınalma fiyatı toplam toleransı** alanına, hesap para birimi cinsinden bir tutar girin. Bu alan yalnızca  **Fiyat toplamlarını eşleştir** alanında **Tutar** veya **Yüzde ve tutar** değeri seçildiğinde kullanılabilir.
13. **Fiyat görüntüleme toplam eşleşmesi simgesi** alanında, fatura eşleştirmesi için bir tutarsızlık toleransı aşarsa bir simge görüntüleme öğesini seçin. Toleransı aşan uyuşmazlık pozitif olduğunda veya pozitif ya da negatif olduğunda simge görüntülenebilir.
Örneğin, tolerans yüzde 5 ve satınalma siparişindeki satır toplam fiyatı 10,00 olsun. Bu nedenle, faturadaki satır toplam fiyatı 10,50'i aştığı takdirde bir fiyat eşleşme simgesi görüntülenir. **Büyükse veya düşükse toleransı**'nı seçerseniz simge, fatura tutarının toplam fiyatının 9,50'ten az olması durumunda da görüntülenir.
13. **Gider eşleştirme**'yi ayarlayın.
14. Gerçek masrafları satınalma siparişi bilgilerine göre beklenen masraflarla eşleştirmek için, **Giderleri eşleştir** onay kutusunu işaretleyin.

## <a name="set-up-unit-price-tolerance-percentages"></a>Birim fiyat toleransı yüzdeleri ayarlama
İzin verilen fiyat tolerans yüzdelerini tanımlamak için **Borç hesapları > Kurulum > Fatura eşleştirme kurulumu > Fiyat toleransı**'na gidin. Satır eşleştirme ilkesi olarak İki yönlü eşleştirme veya Üç yönlü eşleştirme kullanıyorsanız tüzel kişiliğiniz için maddeler ve satıcılar için fiyat toleransı yüzdeleri ayarlayabilirsiniz. Satıcı faturaları, satınalma siparişlerindeki bilgilerle karşılaştırılırken, ilgili fiyat toleransı yüzdesi aranır. Aşağıda varsayılan arama sırası aşağıdaki gibidir:
* Tablo/tablo
* Tablo/Grup
* Tablo/Tümü
* Grup/Tablo
* Grup/Grup
* Grup/Tümü
* Tümü/Tablo
* Tümü/Grup
* Tümü/Tümü

Varsayılan tüzel kişilik fiyat toleransı yüzde 0'dır ve bu fiyat toleransı tüm maddelere ve tüm hesaplara uygulanır (Tümü, Tümü). Varsayılan tüzel kişilik fiyat toleransı kaydını silemezsiniz.

Varsayılan olarak, negatif fiyat uyuşmazlıklarına izin verilir. Ancak, negatif fiyat toleransı yüzdesi giremezsiniz. Negatif fiyat tolerans yüzdelerini izlemek için, **Borç hesabı parametreleri** sayfasındaki **Gider eşleme simgesini göster** alanında **Toleranstan büyükse veya küçükse** seçeneğini belirleyin. Daha sonra **fiyat toleransı** sayfasına fiyat tolerans yüzdeleri girin.

## <a name="set-up-matching-policy-override"></a>Eşleştirme ilkesini geçersiz kılmayı ayarla

**Satın alma siparişi** sayfasındaki satırların **Eşleştirme ilkesi** alanı için varsayılan girişi tanımlamak üzere **Borç hesapları > Kurulum > Fatura eşleştirme kurulumu > Eşleşme ilkesi**'ne gidin. Bu isteğe bağlı bir kurulumdur. Maddeler, satıcılar veya madde ve satıcı birleşimleri için çift-Yön veya üç yönlü eşleştirme ayarlamak üzere bu sayfayı kullanın. Bu girişler, **Borç hesapları parametreleri** sayfasında tanımladığınız yasal varlık eşleştirme ilkesiyle daha fazla parçalı eşleştirme ilkesi tanımlamanızı sağlar. Varsayılan yasal varlık satırı eşleştirme ilkesi, bu sayfada farklı satır eşleştirme ilkesi belirtilmiş olanlar dışındaki tüm madde ve satıcılara uygulanır.

Bu sayfada, **Eşleşen ilke düzeyi** ni seçin. Eşleşen politika sıralamasını belirlemek için eşleşen politika hiyerarşisindeki seviyeyi seçin.

- **Madde ve satıcı** – Belirli satıcılardan satın alınan belirli maddeler için eşleştirme ilkesini belirtin.
- **Madde** – Madde ve satıcı düzeyinde belirtilenler dışında herhangi bir satıcıdan satın alınan belirli maddeler için eşleştirme ilkesini belirtir.
- **SAtıcı** – Madde, satıcı ve madde düzeyinde belirtilenler dışında belirli bir satıcıdan satın alınan belirli maddeler için eşleştirme ilkesini belirtir.
  
Kullanılan eşleştirme ilkesini belirlemek için aşağıdaki hiyerarşi kullanılır:
  *  Madde ve satıcı
  *  Öğe
  *  Satıcı
  *  Tüzel kişilik
  
## <a name="set-up-invoice-totals-matching-tolerance-for-vendors"></a>Satıcılar için fatura toplamları eşleştirme toleranslarını ayarla

Fatura toplamlarının satıcıya özgü toleranslarını belirlemek için **Borç hesapları > Kurulum > Fatura eşleştirme kurulumu > Toplam fatura toleransları**'na gidin. Eşleme hesaplaması, satıcı faturasında sipariş hesabı olarak belirtilen satıcı hesabındaki fatura toplamları tolerans yüzdesini kullanır. Satıcı hesabının fatura toplamları için belirtilmiş bir tolerans yüzdesi yoksa **Borç hesapları parametreleri** sayfasındaki hukuk varlığı için belirtilen fatura toplamları tolerans yüzdesi kullanılır.

1. Varsayılan toleransı geçersiz kılan bağımsız satıcılar için toleransları belirtmek üzere bir **Satıcı hesabı** seçin.
2. Bu satıcı için kabul ettiğiniz fark yüzdesini girin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
