---
title: Stok konumlandırma
description: Bu makalede, sağlama sürelerini kısaltmaya ve tedarik zincirinizdeki şokları emmeye yardımcı olmak için eldeki stoku oluşturabileceğiniz tedarik zincirinizdeki ayırma noktalarını kapsayan stratejik stok konumlandırma hakkında bilgi sağlanmaktadır.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: bec36b5b51b937782afdb78d7009a58dcd0942f0
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186760"
---
# <a name="inventory-positioning"></a>Stok konumlandırma

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Stratejik stok konumlandırma, elinizde stok oluşturabileceğiniz tedarik zincirinizdeki ayırma noktalarını belirlemeyi içerir. Bu yaklaşım esas olarak sağlama sürelerini kısaltmaya ve tedarik zincirinizdeki şokları emmeye yardımcı olmak için kullanılır. Talep değişkenliği tedarik zincirinin sonuna kadar iletilmediği için "kamçı etkisini" azaltmanıza olanak tanır. *kırbaç etkisi* perakende seviyesindeki talepteki küçük dalgalanmaların toptan satış, dağıtıcı, üretici ve hammadde tedarikçisi seviyelerinde giderek daha büyük dalgalanmalara neden olabileceğini ifade eder.

Stok konumlandırma, Talep Temelli Malzeme Gereksinimleri Planlaması'nın (DDMRP) ilk adımıdır.

## <a name="inventory-positioning-for-manufacturing"></a>Üretim için stok konumlandırma

Bu bölümde, tipik bir yastık ürünü üretiyorsanız stok konumlandırma kararlarının nasıl alınacağını gösteren bir örnek sağlanmaktadır. Aşağıdaki resimde gösterildiği gibi yastığın çok düzeyli bir ürün reçetesi (BOM) vardır.

![Yastık ürünü için çok düzeyli ürün reçetesi (BOM) örneği.](media/ddmrp-bom-example.png "Yastık ürünü için çok düzeyli ürün reçetesi (BOM) örneği")

### <a name="choose-your-decoupling-points"></a>Ayırma noktalarınızı seçme

Ayırma noktalarınızı nereye koyacağınızı seçerken, malzeme listesindeki her bir öğenin aşağıdaki tüm yönlerini ölçüt olarak göz önünde bulundurun:

- Harici değişkenlik
- Stok dengeleme ve esneklik
- Kritik işlem koruması
- Müşteri tolerans süresi
- Satış siparişi görünürlük ufku
- Pazar potansiyel sağlama süresi

Yastık örneğinde, aşağıdaki nedenlerle ilk ayırma noktanızı *köpük kütükler*'e koyabilirsiniz:

- Köpük kütükleri yapmak için kullanılan malzemeleri tedarik etmek zordur ve kullanılabilirliği değişkendir. Bu nedenle, *harici değişkenlik* ölçütü karşılanır.
- Köpük kütükler, yastığa ek olarak ürettiğiniz diğer ürünler için köpük ekler oluşturmak üzere birçok farklı şekil ve boyutta kesilebilir. Bu nedenle, *stok dengeleme ve esneklik* ölçütü karşılanır.

Daha sonra bir sonraki ayırma noktanızı önceden kesilmiş yastık kumaşı olan *kumaş kit*'ne koyabilirsiniz. Yalnızca bir kumaş kesme makineniz olduğu için bu noktayı seçebilirsiniz. Bu nedenle *kritik işlem koruma* ölçütü karşılanır.

Son olarak, son ayırma noktanızı bitmiş iyi yastık öğesine koyabilirsiniz. Bu noktayı, satışlarda çok düşük *müşteri tolerans süreniz* olduğu ve *satış siparişi görünürlük ufkunuz* oldukça kısa olduğu için seçebilirsiniz. Bu nedenle, gelen siparişleri karşılamak için eldeki stoka sahip olduğunuzdan emin olmak istersiniz. Ayrıca, teslim süresini bu kadar kısa tutarak daha yüksek bir fiyat belirleyebilirsiniz, *pazar potansiyel sağlama süresi* kriteri bunu ifade eder.

Bu analize dayanarak, aşağıdaki çizim yastık BOM'unun neye benzeyeceğini göstermektedir. Sarı stok sembolleri, ayırma noktalarını vurgular.

![Ayırma noktalarının vurgulandığı örnek BOM.](media/ddmrp-bom-decoupling-example.png "Ayırma noktalarının vurgulandığı örnek BOM")

### <a name="calculate-your-decoupled-lead-time"></a>Ayırma sağlama sürenizi hesaplama

Bu bölümde, ayırma noktalarını ekledikten sonra yeni sağlama sürelerinizi nasıl hesaplayacağınız gösterilmektedir.

Bir önceki bölümde başlatılan yastık örneğine ilişkin aşağıdaki çizimde, sağlama süreleri her bir BOM bileşeninin sol üst kısmındaki gri kutularda gösterilmektedir. Kırmızı ana hat içeren kutular, toplam sağlama süresini (BOM'un her seviyesindeki en uzun tedarik sürelerinin toplamı) yönlendiren ürünleri belirtir. Bu sağlama süresi, sıfırdan başladığınızda 21 gündür.

![Sağlama süreleri ile BOM örneği.](media/ddmrp-bom-lead-times-example.png "Sağlama süreleri ile BOM örneği")

Ancak, daha önce seçtiğiniz ayırma noktalarını uygularsanız, ayrılan ürün her zaman stokta olacaktır. Bu nedenle, 0 (sıfır) bir sağlama süresine sahip olacaklardır. Yastığın yeni sağlama süresi artık sadece beş gündür: ipliğin satın alınması için iki gün ve yastığın üretilmesi için üç gün. Bu hazırlık süresi *ayrılmış sağlama süresi* olarak bilinir.

![Ayrılmış sağlama süresi örneği.](media/ddmrp-bom-decoupled-lead-time-example.png "Ayrılmış sağlama süresi örneği")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Perakende modelinde stratejik stok konumlandırma

Perakendeciler yalnızca bitmiş ürünleri stokladığından, BOM'lar sorun olmaz. Ancak perakendeciler, dağıtım ağındaki depolama konumlarına dayalı olarak stratejik stok konumlandırma ve arabellek seviyeleri ayarlayarak DDMRP'yi kullanmaya devam edebilir.

Aşağıdaki çizimde, Seattle'da bir dağıtım merkezi ve Boston, Atlanta ve Portland'da mağazaları olan bir şirket örneği gösterilmektedir.

![Perakende modelinde konuma dayalı ayırma noktaları.](media/ddmrp-retail-decoupl-points-example.png "Perakende modelinde konum bazında ayrılma noktaları")

Paket ürününü dağıtım merkezi ile mağazalar arasında taşımak için transfer süresinin *müşteri tolerans sürenizi* ihlal ettiğine karar verebilirsiniz, çünkü müşterileriniz ziyaret ettiklerinde paketin stokta olmasını bekler. Bu durumda, üç mağazanın her birinde paket ürünü için bir ayırma noktası kuracaksınız. Her mağaza, sağlama sürelerine, talep modellerine vs. bağlı olarak farklı arabellek seviyelerine sahip olacaktır.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management'ta stok konumlandırmayı uygulama

Bu bölümde, Microsoft Dynamics 365 Supply Chain Management'ta stok konumlandırma stratejinizi nasıl uygulayacağınız açıklanmaktadır.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Ayrılma noktaları oluşturan ürün kapsam gruplarını ayarlama

Ürünler, **Kapsam kodu** değeri *Ayırma noktası* ile yapılandırılmış bir kapsama grubuna ait olduklarında ayırma noktaları olur. Bu nedenle, DDMRP'yi kurma sürecindeki ilk adım, DDMRP stratejiniz için hangi kapsama gruplarını uygulamanız gerektiğine karar vermek ve ardından adımları izleyerek bunları oluşturmaktır.

1. **Master planlama \> Kurulum \> Kapsam \> Kapsam grupları**'na gidin.
1. Kapsam grubu oluşturmak için Eylem Bölmesi'nde **Yeni**'yi seçin.
1. Kapsam grubunu tanımlayan bilgileri girin ve ardından kullanılacak takvimi seçin.
1. **Genel** sekmesinde, **Kapsam kodu** alanını *Ayırma noktası* olarak ayarlayın. Bu ayar, bu kapsama grubuna ait tüm öğelerin DDMRP için ayırma noktaları olarak ele alınmasına neden olur. Ayrıca, bu prosedürde daha sonra açıklandığı gibi, bu grup için tüm DDMRP ayarlarını etkinleştirir.
1. **Diğer** sekmesinde, **DDMRP parametreleri** bölümünde aşağıdaki alanları ayarlayın:

    - **Sağlama süresi faktörü** – Bu kapsam grubundaki kalemler için minimum ve maksimum stok seviyeleri hesaplanırken sağlama süresinin sahip olması gereken etkiyi kontrol etmek için bir faktör (0 ile 1 arasında bir ondalık değer olarak) belirtin. Genel olarak, bir öğenin sağlama süresi ne kadar uzunsa, sağlama süresi faktörü o kadar düşük olmalıdır. Daha düşük bir sağlama süresi faktörü, daha düşük minimum ve maksimum stok seviyeleri üretir ve bu nedenle daha küçük ve daha sık siparişlere neden olur. DDMRP metodolojisi, sağlama süresi uzun olan ürünler için 0,20 ile 0,40 arasında, orta sağlama süresi olan ürünler için 0,41 ile 0,60 arasında ve kısa sağlama süresi olan ürünler için 0,61 ile 1,00 arasında bir değer önerir. Daha fazla bilgi için bkz. [Arabellek profili ve düzeyleri](ddmrp-buffer-profile-and-levels.md).
    - **Değişkenlik faktörü** – Bu kapsam grubundaki ürünler için minimum stok seviyesi hesaplandığında değişen talebin sahip olması gereken etkiyi kontrol etmek için bir faktör (0 ile 1 arasında bir ondalık değer olarak) belirtin. Genel olarak, bir ürünün talebi ne kadar değişkense, değişkenlik faktörü o kadar yüksek olmalıdır. Daha yüksek değişkenlik faktörü, daha yüksek minimum stok seviyesi üretir. DDMRP metodolojisi, düşük değişkenliğe sahip ürünler için 0,00 ile 0,40 arasında, orta değişkenliğe sahip ürünler için 0,41 ile 0,60 arasında ve yüksek değişkenliğe sahip ürünler için 0,61 ile 1,00 arasında bir değer önermektedir. Daha fazla bilgi için bkz. [Arabellek profili ve düzeyleri](ddmrp-buffer-profile-and-levels.md).
    - **Min, maks ve yeniden sipariş noktası dönemi** – Arabellek değerlerinin ne sıklıkta hesaplanacağını belirtin (*Günlük* veya *Haftalık*).

1. **Diğer** sekmesinde, **Ortalama günlük kullanım** bölümünde aşağıdaki alanları ayarlayın:

    - **Ortalama günlük kullanıma dayalı** – Ortalama günlük kullanım (ADU) hesaplamasının hangi zaman periyotlarına dayanacağını seçin. Aşağıdaki değerlerden birini seçin:

        - *Geçmiş* – **Geçmiş dönem (günler)** alanında belirtilen gün sayısı için yalnızca geçmiş kullanıma bakın. ADU, hesaplama döneminde (stok birimlerinde) bir ürün için toplam talebin hesaplama dönemindeki gün sayısına bölünmesiyle hesaplanır.
        - *İleri* – **İleri dönem (günler)** alanında belirtilen gün sayısı için yalnızca tahmini gelecek kullanıma (tahminler dahil) bakın. ADU, hesaplama döneminde (stok birimlerinde) bir ürün için toplam talebin hesaplama dönemindeki gün sayısına bölünmesiyle hesaplanır. 
        - *Karışık* – Hem geçmiş hem de gelecekteki kullanıma bakın. **Geçmiş dönem (günler)**, **İleri dönem (günler)** alanları ve karışık seçeneklerinin tümü uygulanır. 

            *Karışık ADU* = (\[*Geçmiş ağırlıklandırma* × *Geçmiş ADU*\] + \[*İleri ağırlıklandırma* × *İleri ADU*\]) ÷ (*Geçmiş ağırlıklandırma* + *İleri ağırlıklandırma*)

    - **Geçmiş dönem (günler)** – Sistemin bu kapsam grubundaki ürünlerin ADU'sunu hesaplarken dikkate alması gereken geçmiş günlerin sayısını (bugüne kadar ve dahil) girin. Bu ayar yalnızca **Ortalama günlük kullanım temel alınarak** alanı *Geçmiş* veya *Karışık* olarak ayarlandığında geçerlidir.
    - **İleri dönem (günler)** – Sistemin bu kapsama grubundaki ürünlerin ADU'sunu hesaplarken dikkate alması gereken gelecek günlerin sayısını (bugünden belirtilen güne kadar) girin. Bu ayar yalnızca **Ortalama günlük kullanım temel alınarak** alanı *İleri* veya *Karışık* olarak ayarlandığında geçerlidir.
    - **Karışık ortalama günlük kullanım için geçmiş dönemin göreli ağırlığı** – Karışık ADU hesaplanırken geçmiş döneme uygulanacak ağırlığı (yüzde olarak) girin. Bu ayar yalnızca **Ortalama günlük kullanıma göre** alanı *Karışık* olarak ayarlandığında uygulanır.
    - **Karışık ortalama günlük kullanım için ileri dönemin göreli ağırlığı** – Karışık ADU hesaplandığında ileri döneme uygulanacak ağırlığı (yüzde olarak) girin. Bu ayar yalnızca **Ortalama günlük kullanıma göre** alanı *Karışık* olarak ayarlandığında uygulanır.

1. Diğer tüm sekmeler ve alanlar için, bu kapsam grubuna bağlı ürünlere ilişkin gereksinimleri hesaplamak için kullanılan ayrıntılı ayarları girin.

### <a name="set-an-item-as-a-decoupling-point"></a>Öğeyi ayırma noktası olarak ayarlama

Öğeyi ayırma noktası olarak ayarlamak için aşağıdaki adımları izleyin.

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. DDMRP için ayarlamak istediğiniz serbest bırakılan ürünü bulun ve seçin.
1. Eylem Bölmesi'nin **Plan** sekmesinde **Öğe kapsamı**'nı seçin.
1. **Ürün kapsamı** sayfasında, her biri farklı bir depolama ve ürün boyutları kombinasyonu için geçerli olan birkaç madde kapsamı kaydı zaten listelenmiş olabilir. Ayırma noktası oluşturmak istediğiniz boyutlar için geçerli olan mevcut bir ürün kapsamı kaydını seçebilirsiniz. Alternatif olarak, yeni ürün kapsamı kaydı oluşturmak için Eylem Bölmesi'nde **Yeni** öğesini seçebilirsiniz.
1. Ürün kapsamı kaydını her zamanki gibi ayarlayın. En azından, ayırma noktasının uygulanacağı siteyi ve depoyu belirtmelisiniz.
1. Uygun kayıt seçiliyken **Genel** sekmesini seçin.
1. **Belirli ayarları kullan** onay kutusunu seçin.
1. **Kapsam grubu** alanını, ayırma noktaları oluşturmak üzere ayarlanmış bir kapsama grubuna ayarlayın (önceki bölümde açıklandığı gibi).
1. Ürün artık bir ayırma noktası olarak yapılandırılmıştır. Genellikle, DDMRP kullandığınızda, burada arabellek boyutlarını ve yeniden sipariş miktarını etkileyen ayarları da yapılandırırsınız. Bununla birlikte, yapılandırmayı daha sonra tamamlayabilirsiniz. (Daha fazla bilgi için bkz. [Ayırma noktası ürünü için arabellekleri ayarlama](ddmrp-buffer-profile-and-levels.md#set-up-buffers).)

> [!NOTE]
> Ayırma noktası olmayan ürünleri planlamak için standart malzeme gereksinimleri planlaması (MRP) kullanıldığında izlediğiniz adımların aynısını izleyin.
