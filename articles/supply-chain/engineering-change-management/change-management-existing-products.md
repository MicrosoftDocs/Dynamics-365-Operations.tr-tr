---
title: Mevcut ürünlerde değişiklik yönetimini etkinleştirme
description: Bu konuda, var olan ürünler için değişiklik yönetimini nasıl etkinleştirebileceğiniz açıklanmaktadır. Ayrıca, değişiklik yönetimini etkinleştirme yeteneğinizin sınırlı olduğu durumları da açıklar.
author: t-benebo
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e356ef8339f8f71965bf9313e14fed3d0810152d
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103625"
---
# <a name="enable-change-management-on-existing-products"></a>Mevcut ürünlerde değişiklik yönetimini etkinleştirme

[!include [banner](../../includes/banner.md)]

Bu konuda, var olan ürünler için değişiklik yönetimini nasıl etkinleştirebileceğiniz açıklanmaktadır. Ayrıca, değişiklik yönetimini etkinleştirme yeteneğinizin sınırlı olduğu durumları da açıklar.

Var olan bir ürün için değişiklik yönetimini etkinleştirdiğinizde, bu ürünün sürümlerini oluşturabilir ve üründe yapılan değişiklikleri kullanım ömrü boyunca izleyebilirsiniz. Bu nedenle, değişiklik emirlerini kullanarak bu değişiklikleri izleyebilirsiniz. Değişiklik yönetimini etkinleştirmek için ilgili ürünleri *mühendislik öğelerine* (mühendislik ürünleri olarak da adlandırılır) dönüştürmeniz gerekir. Mühendislik ürünleri, değişiklik yönetimi yoluyla sürümü oluşturulan ve yönetilen ürünlerdir. Dönüştürme işleminde size yol gösterecek bir sihirbaz sağlanmıştır.

## <a name="turn-this-feature-on-or-off"></a>Bu özelliği açma veya kapatma

Bu konuda açıklanan işlev, sisteminiz için hem *Mühendislik Değişiklik Yönetimi* hem de *Mevcut ürünlerde değişiklik yönetimini etkinleştir* özelliğinin açık olmasını gerektirir. Bu özelliklerin nasıl açılacağı veya kapatılacağı hakkında ayrıntılar için bkz. [Mühendislik değişiklik yönetimine genel bakış](product-engineering-overview.md).

## <a name="restrictions-and-limitations"></a>Kısıtlamalar ve sınırlamalar

Tüm ürün türleri diğer tüm türlere dönüştürülemez. Aşağıdaki kısıtlamalar ve sınırlamalar geçerlidir:

- Bir ürünü mühendislik ürününe dönüştürdüğünüzde, *ürün* olarak kalır. Bir *ana ürün* olmaz.
- Belirli bir boyut kümesine sahip bir ürün yöneticisini dönüştürdüğünüzde, bu boyutlar değişiklik sonrasında korunur. Örneğin, boyut boyutuna sahip bir ürün yöneticisini dönüştürürseniz boyut boyutu korunur.

Bu nedenle, farklı bir ürününüz varsa bunu yalnızca hareketlerdeki ürün boyutunu izlemeyen bir mühendislik ürünüyle değiştirebilirsiniz (diğer bir de misli sürüm boyutu kullanılmaz). Bu sorunlar hakkında daha fazla bilgi için bu konunun diğer bölümlerine bakın.

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a>Gerekli tüm mühendislik ürün kategorilerini oluşturarak dönüşüme hazırlanma

Her mühendislik ürününe bir *mühendislik ürünü kategorisi* atanmalıdır. Bu atamayı **Mühendislik ürününe dönüştür** sihirbazını çalıştırdığınızda yaparsınız. Bu ürünleri dönüştürmeden *önce* ilgili tüm standart ürünler için mühendislik ürün kategorileri bulunmalıdır.

Mühendislik ürünü kategorisi, bir mühendislik ürünü oluşturmak için temel oluşturur ve bir dizi varsayılan değer ve ilke oluşturur. Mühendislik öznitelikleri ve bunların varsayılan değerleri (mühendislik kategorisi için tanımlandığı üzere) elde edilen mühendislik ürününe de uygulanır. Öznitelik değerlerini düzenleyebilir ve/veya gerektiğinde elde edilen ürüne daha fazla mühendislik özniteliği ekleyebilirsiniz.

Mühendislik ürünü kategorisi, atadığınız ürünle eşleşmelidir. Örneğin, ürün türü ve boyut grubu hem ürün hem de mühendislik ürünü kategorisiyle eşleşmelidir. Daha fazla bilgi için bkz. [Mühendislik sürümleri ve mühendislik ürünü kategorileri](engineering-versions-product-category.md).

> [!IMPORTANT]
> **Mühendislik ürününe dönüştür** sihirbazı, ürünü yalnızca sürümün hareketlerde izlenmediği mühendislik ürünlerine dönüştürebilir. Bu nedenle, var olan ürünleri dönüştürmek için oluşturduğunuz mühendislik ürünü kategorileri için **Hareketlerdeki sürümü izle** seçeneğini *Hayır* olarak ayarlanmalıdır.

Mühendislik ürünü kategorileri oluşturma hakkında bilgi için bkz. [Mühendislik sürümleri ve mühendislik ürünü kategorileri](engineering-versions-product-category.md).

## <a name="run-the-convert-to-engineering-product-wizard"></a>Mühendislik ürününe dönüştür sihirbazını çalıştırma

**Mühendislik ürününe dönüştür** sihirbazı, var olan bir veya daha fazla ürünü mühendislik ürünlerine dönüştürmenize yardımcı olur. Ürünleri, sürümün işlemlerde izlenmediği (yani sürüm boyutunun kullanılmadığı) mühendislik ürünlerine (sürümü oluşturulmuş ürünler) dönüştürür. Dönüştürme tamamlandıktan sonra, Mühendislik değişikliği yönetimi'ni kullanarak ürünleri yönetebilirsiniz.

Dönüştürme işlemi kalıcıdır. Bu nedenle, daha sonra tersine çeviremezsiniz. 

Dönüştürülen her mühendislik ürünü, orijinal ürünün serbest bırakıldığı şirketlerde serbest bırakma işlemi devam edecektir. Ancak, mühendislik ürün reçetesi ve rotalar bu şirketlere otomatik olarak yayınlanmaz.

**Mühendislik ürününe dönüştür** sihirbazını çalıştırmak ve bir ürünü mühendislik ürününe dönüştürmek için aşağıdaki adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Kılavuzda, dönüştürmek istediğiniz her ürün için onay kutusunu seçin.
1. Eylem Bölmesinde, **Mühendis** sekmesinde, **Mühendislik değişikliği yönetimi** grubunda, **Mühendislik ürününe dönüştür**'ü seçerek sihirbazı açın.
1. Sihirbazın ilk sayfası **Hoş Geldiniz** sayfasıdır. Dönüştürme işlemi hakkında bilginiz yoksa bu sayfadaki bilgileri dikkatlice okuyun. Devam etmeye hazır olduğunuzda **İleri**'yi seçin.
1. **Dönüştürülecek ürünlerin ayrıntılarını seçin** sayfası, sihirbazı açmadan önce seçtiğiniz her ürünü gösterir. Listeyi inceleyin. Ürünleri istediğiniz gibi eklemek veya kaldırmak için araç çubuğundaki **Yeni** ve **Sil** düğmelerini kullanın.
1. Listelenen her ürüne varsayılan değerler atamak için kılavuzun üst kısmında yer alan aşağıdaki alanları kullanın. (Dönüştürme tamamlandıktan sonra ürünler için bu değerleri tek tek değiştirebilirsiniz.) Varsayılan değerler, ilgili değerin atandığı ürünlere atanmayacaktır.

    - **Varsayılan mühendislik kategorisi**: Listelenen her ürüne atamak için bir başlangıç mühendislik ürün kategorisi seçin. Seçtiğiniz kategori yalnızca onunla uyumlu ürünlere uygulanır.
    - **Varsayılan sürüm** Listelenen her ürüne atanacak ilk ürün sürümünü girin. Her mühendislik ürününün en az bir mühendislik versiyonu vardır.
    - **Varsayılan yaşam döngüsü durumu**: Listelenen her ürüne atanacak ilk ürün yaşam döngüsü durumunu seçin.
    - **Geçerli ürün reçetesi mühendislik ürününün bir parçası olacaktır**: Listelenen her ürün için geçerli ürün reçetesinin mühendislik ürünü için ürün reçetesi olarak kullanılması gerekiyorsa bu onay kutusunu işaretleyin.

    Ürün ayarları hakkında daha fazla bilgi için sonraki adıma bakın.

1. Kılavuzda listelenen her ürünü gözden geçirin ve atadığınız varsayılan değerlerin ürüne ne kadar iyi uygulandığını değerlendirin. Her satır için aşağıdaki bilgileri gözden geçirin ve ilgili alanları ayarlayın:

    - **Ürün numarası**: Ürün numarası.
    - **Ürün adı**: Ürünün adı.
    - **Mühendislik kategorisi**: Ürünün dönüştürüldükten sonra ait olması gereken mühendislik ürünü kategorisini seçin. Bu konunun önceki bölümünde açıklandığı gibi, her ürün için uygun bir kategori zaten mevcut olmalıdır. Her ürüne bir kategori atamanız gerekir.
    - **Sürüm**: Dönüştürüldükten sonra ürüne atanacak ürün sürümünü girin. Örneğin, kategorinizin zaten kullandığı numara serisine uyan bir sayı seçebilirsiniz. Her mühendislik sürümü, bu sürüme özgü mühendislikle ilgili verileri depolar. Daha fazla bilgi için bkz. [Mühendislik sürümleri ve mühendislik ürünü kategorileri](engineering-versions-product-category.md).
    - **Ürün yaşam döngüsü durumu**: Ürünün dönüştürüldükten sonra içinde olması gereken ürün yaşam döngüsü durumunu seçin. Ürün yaşam döngüsü durumu, belirli bir mühendislik sürümü için hangi işlemlere izin verildiğini denetlemenizi sağlar. Daha fazla bilgi için bkz. [Ürün yaşam döngüsü durumları ve hareketler](product-lifecycle-state-transactions.md).
    - **Ürün reçetesi var**: Seçili onay kutusu ürünün, ürün reçetesine sahip olduğunu gösterir. Bu onay kutusunun ayarı, **Geçerli ürün, reçetesi mühendislik ürününün bir parçası olacak** ayarını nasıl yapacağınıza karar vermenize yardımcı olabilir.
    - **Geçerli ürün reçetesi, mühendislik ürününün bir parçası olacak**: Ürünün geçerli ürün reçetesinin mühendislik ürünü için ürün reçetesi olarak kullanılması gerekiyorsa bu onay kutusunu işaretleyin. Bu ürün reçetesi daha sonra Mühendislik değişikliği yönetimi tarafından yönetilecektir. Ürünün ürün reçetesi yoksa veya dönüştürülen ürün için daha sonra el ile ürün reçetesi oluşturmayı tercih ediyorsanız bu onay kutusunu temizleyin.
    - **Hatalar var**: Seçilen onay kutusu, ürün kurulumunda bir veya daha fazla hata olduğunu gösterir. Örneğin, ürün türü veya boyut grubu kategoride eşleşmeyebilir. Hata olan ürünler atlanacak ve dönüştürülmeyecektir.

1. İşiniz bittiğinde, ürün kurulumunu doğrulamak için araç çubuğunda **Doğrula**'yı seçin. Her satır için **Hatalar var** onay kutusu ürünün durumunu belirtmek üzere güncelleştirilir. Her ürünün kurulumu hatasız olana kadar değerleri ayarlayın.
1. Tüm ürünler doğru ayarlandığında, devam etmek için **İleri**'yi seçin.
1. **Seçimi onayla** sayfası, kurulumunda hata olmayan ve bu nedenle dönüştürmeye hazır olan ürünlerin sayısını gösterir. Ayrıca, hatalar nedeniyle atlanacak ürün sayısını da gösterir. Dönüştürmeyi toplu işlem olarak çalıştırmak için **Toplu iş çalıştır** seçeneğini *Evet* olarak ayarlayın.
1. Ayarlarınızı uygulamak ve ürünleri mühendislik ürünlerine dönüştürmeye başlamak için **Bitir**'i seçin.

> [!NOTE]
> Sisteminiz ürünleri serbest bırakılmadan önce el ile kabul etmek üzere ayarlanmışsa dönüştürülen her ürünü uygun şirketlerde **Ürün sürümlerini aç** sayfasını kullanarak kabul etmelisiniz. Daha fazla bilgi için bkz. [Ürünü yerel şirkette serbest bırakmadan önce gözden geçirme ve kabul etme](engineering-scenarios.md#accept).
