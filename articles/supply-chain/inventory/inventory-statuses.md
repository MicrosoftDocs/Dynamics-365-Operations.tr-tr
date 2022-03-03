---
title: Stok durumları
description: Bu makalede, stoğu kategorilendirmek ve izlemek için stok durumlarını nasıl kullanabileceğiniz açıklanmaktadır.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db15ad94355823c699e83c9e3f47660f813e1c9a
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103475"
---
# <a name="inventory-statuses"></a>Stok durumları

[!include [banner](../includes/banner.md)]

Bu makalede, stoğu kategorilendirmek ve izlemek için stok durumlarını nasıl kullanabileceğiniz açıklanmaktadır.

## <a name="set-up-and-use-inventory-statuses"></a>Stok durumlarını ayarlama ve kullanma

Stok durumlarını stoku kategorilere ayırmak için kullanabilirsiniz. Arından stok yenileme veya yerine koyma gibi uygun eylemleri başlatabilirsiniz.

Burada stok durumlarını kullanabileceğiniz bazı yollara ilişkin örnekler verilmiştir:

- Eldeki stok, gelen hareketler ve giden hareketler için stok durumları oluşturun.
- Ambar hareketleri için varsayılan bir stok durumu belirleyin.
- Teslim almadan, teslim alırken veya maddeler stok hareketi sırasında yerine konulurken maddelerin stok durumunu değiştirin.
- İade edilen maddeleri fiyatlandırmak ve master planlama sırasında madde karşılama planlamak için stok durumunu kullanın.

Stok durumu, depolama boyutu grubundaki boyutlardan biridir. Stok durumları, kullanılabilir veya kullanılamaz diye kategorilere ayrılabilir ve kullanılmayan bir stok durumuna sahip olan maddeleri engellemek için **Stok engelleme** parametresini kullanabilirsiniz. Engellenen bir duruma sahip olan maddeler fiziksel stok olarak kabul edilir ve bir üretim emri, satış emri, transfer emir veya giden hareket üzerinde kullanılamaz.

Gelen iş için kullanılabilir veya kullanılamaz stok durumuna sahip ambar maddelerini kullanabilirsiniz. Örneğin, *Hazır* adında bir kullanılabilir durum, *Hasarlı* adında bir kullanılamayan durum ve *Engelli* adında bir engellenen durum oluşturuyorsunuz. Alınan veya iade edilen madeler için bir satın alma emri oluşturduğunuzda maddeler hasarlı veya arızalı ise bu maddelerin stok durumunu satın alma emri satırında *Hasarlı* olarak değiştirebilirsiniz. Bu maddeler teslim alındıktan sonra durum otomatik olarak *Engelli* olarak ayarlanır. Hasarlı maddeleri bir taşınabilir cihaz kullanarak tarıyorsanız Supply Chain Management bu maddeleri yerine koyabileceğiniz uygun bir konum veya konumlar hakkında bilgi göstermek üzere konum direktiflerini ve iş şablonlarını kullanabilir. İade edilen maddeler için *Stok hareketleri* sayfasında **Rezervasyon** türü bir sorun oluşturulur.

**Stok durumları** sayfasındaki **Stok durdurma** onay kutularını kullanarak hangi stok durumlarının durdurulacağını belirtebilirsiniz. Satış siparişleri, transfer emirleri veya proje tümleştirmeleri için stok durumlarını durdurma durumları olarak kullanamazsınız.

Giden işe için hangi stoğun rezerve edilecek olduğunu denetlemek için farklı engellemeyen stok durumları kullanabilirsiniz. *Engelleniyor* durumunda olan maddeler varsa ve master planlama bu maddeler üzerinde çalıştırılıyorsa maddelerin eksik olduğu kabul edilir ve stok otomatik olarak yenilenir. Ayrıca, giden işle ilişkili kalite emirleri için, kalite emri doğrulamasının bir parçası olarak **stok durumu** güncelleştirilemez.

> [!NOTE]
> Açık çalışmanın bulunduğu konumlarda stokun durumunu değiştiremezsiniz. Örneğin, bir madde için satın alma alım işlemi yaptıysanız ancak yerine koyma adımını yapmadıysanız alıcı konum için açık çalışma bulunur ve bu konumdaki stokun durumunu değiştirmeye çalışırsanız bir hata alırsınız. İlgili çalışmayı tamamlamak veya iptal etmek durumu değiştirmenize olanak sağlar.
>
> Genellikle, açık ambar çalışması ile ilgili eldeki stokların durumu yalnızca ambar yönetimi mobil uygulamasını kullanan çalışanlar tarafından değiştirilir, örneğin, bir taşıma işlemi yürütülürken.

Stok durumlarını oluşturduktan sonra bir saha, madde ve ambar için varsayılan stok durumunu ayarlayabilirsiniz. Ayrıca satışlar, transferler ve satın alma emirleri için de varsayılan bir durum ayarlayabilirsiniz. Satış emirleri ve giden transferler için varsayılan durumun **Stok engelleme** seçeneğini *Evet* olarak ayarlanamaz. Bir saha, ambar, madde, satın alma emri, transfer emri veya satış emri ile ilgili varsayılan ayarlardan gelen stok durumu taşınabilir aygıt kullanarak veya satın alma emir, satış emri veya transfer emri satırında değiştirilebilir.

Bir kullanılabilen stok durumuna sahip maddelerin karşılanmasını planlamak için **Depolama boyutu grupları** sayfasında bir depolama boyutu için **Boyuta göre karşılama planı** seçimini yapın. **Madde Karşılama** sihirbazını açtığınızda, bir kullanılabilir duruma sahip olan maddeler **Durum** sayfasında görüntülenmez. Bu maddeler için karşılama ayarları oluşturmak için kullanılabilen stok durumları için stok durumu kimliğini seçin. Karşılama ayarlarına bağlı olarak, madde gereksinimlerini hesaplayabilir ve master planlama sırasında kullanılabilir maddelerin arz ve taleplerini tahmin edebilirsiniz. Bir engelli stok durumuna sahip bir madde karşılama kurulumu oluşturamazsınız. Alternatif olarak, madde karşılama parametreleri oluşturmak veya bunları değiştirmek için **Madde karşılama** sayfasını kullanın.

## <a name="change-inventory-statuses"></a>Stok durumlarını değiştirme

Stok durumlarını, **Konuma göre eldeki** sayfasını kullanarak veya *Stok durumu değişikliği* periyodik görevini kullanarak değiştirebilirsiniz.

- *Stok durumu değişikliği* periyodik görevini kullanırken, dahil edilecek kayıtları seçebilir ve görevi, toplu işte istenen zaman aralığında çalışacak şekilde ayarlayabilirsiniz.
- Stok durumunu geçici bir işlem olarak değiştirmek için **Konuma göre eldeki** sayfasına gidin, ilgili kayıtları seçin ve **Stok durumu değişikliği** düğmesini seçin.

> [!NOTE]
> *İzleme boyutlarına göre denetlenen maddelerin stok durumunu değiştir* özelliği, yalnızca seçili kayıtları güncelleştirme yeteneği de dahil olmak üzere, izleme boyutlarına göre denetlenen maddelerin stok durumunu değiştirmenize olanak tanır. Supply Chain Management 10.0.25 itibarıyla, bu özellik zorunludur ve kapatılamaz. 10.0.25 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *İzleme boyutları tarafından denetlenen maddelerin stok durumunu değiştir* özelliğini aratarak bu işlevi açabilir veya kapatabilir. Özellik etkinleştirildiğinde, aşağıdakileri yapabilirsiniz:
>
> - **Konuma göre eldeki** sayfasında, **Boyutları görüntüle** düğmesini kullanarak satırları gösterilen boyutlara göre gruplandırabilir ve seçili satırların durumunu değiştirebilirsiniz.
> - **Konuma göre eldeki** sayfasında, birden fazla kayıt seçebilir ve Tümünü bir seferde değiştirmek için **Stok durumu değişikliği** düğmesini kullanabilirsiniz.
> - **Stok durumu değişiklik** periyodik görevinde izleme boyutlarına göre filtre uygulayabilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
