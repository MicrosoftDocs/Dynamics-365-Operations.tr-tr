---
title: Yıl sonu kapanışı
description: Bu başlık, genel muhasebe yıl sonu kapatma işlemini çalıştırmak için gerekli kurulum ve adımları açıklar.
author: kweekley
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04eeb8886d74fa8c633d2ac4e9e47aa28a12ee30
ms.sourcegitcommit: e06b7d4de6d5ee7ae491d437d6c0365608a5380b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2021
ms.locfileid: "7892489"
---
# <a name="year-end-close"></a>Yıl sonu kapanışı

[!include [banner](../includes/banner.md)]

Bu başlık, genel muhasebe yıl sonu kapatma işlemini çalıştırmak için gerekli kurulum ve adımları açıklar.

Bir mali dönem sonunda, açılış bakiyelerini yeni yıla aktarmak için yıl sonu kapanış sürecini yürütmeniz gerekir. Çoğu kuruluş yıl sonu kapatma işlemini birden çok kez yürütür. İlk çalıştırma bakiyeleri yeni mali yıla taşır. İşlem daha sonra, bakiyeleri girişleri ayarlamaktan yeni mali yıla taşımak için gerektiği kadar yeniden çalıştırılabilir.

Yıl sonu kapatma işlemi sırasında, olası hareketlerin iki türü oluşturulur. Bir Açılış hareketi her zaman oluşturulur ve açılış bakiyesini yeni mali yılda oluşturmak için kullanılır. Açılış hareketi, bilanço genel muhasebe hesap defteri bakiyelerini yeni mali yılda gösterir ve kar ve zarar genel muhasebe defteri bakiyelerini kalan gelirler genel muhasebe defteri hesabında yeni mali yılda dengeler. Kapanış hareketi, kapatılan mali yıldaki kar ve zarar hesaplarının bakiyesini sıfıra indirmek için isteğe bağlı oluşturulur.

## <a name="prepare-to-run-the-year-end-close"></a>Yıl sonu kapamayı çalıştırmaya hazırlamak

Yıl sonu kapanış işlemini çalıştırmadan önce, aşağıdakiler için ayarları doğrulayın:

**Ana hesap** sayfasında:

- **Ana hesap türü** alanının her ana hesap için doğru ayarlı olduğunu doğrulayın. Ana hesap türü, ana hesabın bakiyesinin bir açılış bakiyesi olarak mı yoksa kapalı olarak mı kalan gelirlere Açılış hareketinde ileri taşınacağı belirler.
- Ana hesabın bakiyesi yıl sonu kapanışı sırasında yeni bir ana hesaba aktarılabilir. Yeni ana hesabı, **Açılış hesabı** alanına girin. Genellikle bu alan, bilanço ana hesapları için, ana hesap devre dışı bırakıldığında ve yeni bir ana hesap, yeni mali yıl için kullanıldığında kullanılır.

**Genel muhasebe parametreleri** sayfasında **Mali yıl kapanışı** altında:

- Önceki yıl sonu kapanışından sistem tarafından oluşturulan açılış hareketinin silinip silinmeyeceğini belirtmek için **Yıl sonu kapanışı yeniden çalıştırıldığında var olan yıl sonu girişlerini sil** seçeneği kullanılır. Bu seçenek **Evet** olarak ayarlanırsa önceki açılış ve isteğe bağlı kapanış hareketleri silinir ve yeni bir açılış veya kapanış hareketi geçerli bakiyelere göre oluşturulur. Bu seçenek **Hayır** olarak ayarlanırsa önceki açılış ve isteğe bağlı kapanış hareketleri kalır ve ek bir açılış ve kapanış hareketi, bakiyeleri ileriye doğru, önceki yıl kapanışı hareketlerinden ileriye doğru ayarlamak için oluşturulur.
- **Aktarma sırasında kapanış hareketleri oluştur** seçeneği, tüm ana hesaplara ait bakiyeleri 0 (sıfır) durumuna getirmek için kapatılan mali yılın kapanış hareketlerini oluşturması için kullanılır. Bu seçenek **Evet** olarak ayarlanırsa hem açılış hareketi hem de kapanış hareketi oluşturulur. Bu seçenek **Hayır** olarak ayarlanırsa yalnızca açılış hareketi bir sonraki mali yılda, bakiyeleri aktarmak için oluşturulur. Ana hesap bakiyeleri, mali yılın sonunda kalır.
- **Mali yıl durumunu kalıcı kapalı olarak ayarlama** seçeneği, mali yılı kalıcı olarak kapalı duruma ayarlamak için kullanılır. Kalıcı olarak kapatılmış durumundaki dönemler yeniden açılamadığı için bu seçeneği dikkatli kullanın. Bu nedenle, düzeltmeler mali yıla nakledilemez. En iyi uygulama olarak, bu seçenek **Hayır** olarak ayarlanmalıdır.
- **Makbuz numarası doldurulmalıdır** seçeneği kaldırıldı. Yıl sonu kapatma işlemi çalıştırıldığında artık bir fiş gereklidir. O sırada makbuz numarası el ile girilir.

**Mali takvim** sayfası üzerinde:

- Yıl sonu kapanışını çalıştırmadan önce bir sonraki mali mevcut olmalıdır. Aksi takdirde, başlangıç bakiyeleri açılış döneminde oluşturulamaz.

**Genel muhasebe takvimi** sayfasında:

- İsteğe bağlı: Yeni hareketlerin girilmesini önlemek için kapatılan mali için her mali dönem **Tutulan** olarak ayarlanabilir. Ayarlama girdileri tanımlandıktan sonra, düzeltme girişlerini deftere nakletmek için tutulan dönemler yeniden açılabilir, yıl sonu kapanış işlemi çalıştırılmış olsa bile.

**Yıl sonu kapanış şablonu kurulumu** sayfasında:

- **Genel muhasebe yıl sonu iyileştirmeleri** özelliği açıldığında, yıl sonu kapanış şablonunun ayarlama işlemi yıl sonu kapanışını çalıştırma işleminden ayrılır. Şablon, **Yıl sonu kapanış şablonu kurulumu** sayfasında **(Genel muhasebe \> Defter kurulumu \> Yıl sonu kapanış şablonu kurulumu)** tanımlanabilir veya yıl sonu kapanış işleminden erişilebilir.

## <a name="define-year-end-close-templates"></a>Yıl sonu kapanış şablonlarını tanımlama

Sistem yapılandırıldıktan sonra, yıl sonu kapanış işlemi çalıştırılabilir. **Yıl sonu kapanış şablonu kurulumu** sayfası üzerinde, yıl sonu kapanışının çalıştırılacağı tüzel kişilikler grubu için bir şablon tanımlanabilir. Bu şablon, her yıl sonu kapanışında yeniden kullanılır ancak kuruluşunuz değişim gösterirse değiştirilebilir.

Öncelikle, şablon için **Grup adı** ayarlayın ve mali takvimi seçin. Grup adı, tüzel varlıkların dahil olduğu grubu tanımlamalıdır. Tüzel kişilik gruplarını belirlerken, tüzel kişiliklerin yalnızca aynı mali takvim seçilirse aynı gruba dahil edilebileceğini unutmayın. Örneğin, şablonlar coğrafyaya göre ayarlanabilir ve Kuzey Amerika tüzel kişilikleri, Avrupa, Orta Doğu ve Afrika (EMEA) tüzel kişilikleri ile Asya-Pasifik (APAC) tüzel kişilikleri için ayrı gruplar oluşturulabilir.

Ardından, tüzel varlıklar şablona eklenebilir. Tüzel varlıklar, bir kuruluş hiyerarşisi seçerek veya tüzel varlıkları seçerek eklenebilir. Bir kuruluş hiyerarşisi seçilirse, sadece bu hiyerarşi içerisindeki, bu seçili mali takvimi kullanan tüzel varlıklar şablona eklenecektir. Tüzel varlıkları şablona eklemek için kullanırsanız, sadece aynı mali takvimi kullanan tüzel varlıklar eklenebilir. Yıl sonu kapanışı, takvimden takvime farklılık gösterebilen bir mali yıl seçilerek çalıştırıldığı için aynı mali takvim kullanılabilir.

Tüzel varlıklar eklendikten sonra, her bir tüzel varlık için kalan kazançlar ana hesaplarını tanımlayın.

**Mali boyut** sekmesi, açılış hareketinde kullanılacak mali boyutları tanımlamak için kullanılır. Bu sekmedeki kurulumun yalnızca **Tüzel Kişilikler** kılavuzunda seçilen tüzel kişilik için geçerli olduğunu unutmayın. Kılavuzdaki her tüzel varlık için kurulumu tekrar etmeniz gerekir.

**Transfer bilanço boyutları** seçeneği, bilanço hesaplarına nakledilen hareketlerdeki finansal boyutların, açılış hareketinde tutulup tutulmayacağını belirlemek için kullanılır. En iyi uygulama olarak bu seçenek **Evet** olarak ayarlanmalıdır. Bilanço boyutlarının ayarı, tutulan kazanç genel muhasebe hesaplarındaki mevcut bakiyeleri etkilemez. Bu bakiyeler, bir sonraki bölümde tanımlanan kar ve zarar boyutlarına göre belirlenir. Örneğin, 2019 mali yılı kapatılan ilk yıldır ve kapanış için **Departman** ve **Maliyet merkezi** boyutlarını seçmek üzere **Tümünü kapat** seçeneği kullanılmıştır. Bu durumda, bir departman ve maliyet merkezinin her kombinasyonu için ayrı bir birikmiş kar hesabı oluşturulmuştur. Yıl sonu kapanışı 2020 mali yılı için çalıştırıldığında, **Bilanço boyutlarını aktar** **Hayır** olarak ayarlanmış olsa bile, önceki yılın birikmiş kazançları tam olarak deftere nakledildikleri gibi kalır. Önceki yıl sonu kapanışlarından elde edilen kazançlara nakledilen bakiyeler hiçbir zaman değiştirilmez.

**Kar ve zarar boyutlarını aktar**, kar ve zarar hesaplarına nakledilmiş olan hangi finansal boyutların, kalan gelirler ana hesabına aktarılacağını belirlemek için kullanılır. Öncelikle, hangi finansal boyutların seçilen tüzel varlıkla ilişkili olduğunu tanımlayın. Bu mali boyutlar, mali boyut etkin bir hesap yapısının parçası olmasa bile, yıl içinde deftere nakledilen tüm mali boyutları içerir. Daha sonra, her bir boyutu **Kapalı tek** veya **Tümü kapalı** olarak tanımlayın. Varsayılan seçenek **Tümünü kapat**'tır. Bu seçenek, deftere nakledilen hareketlerdeki özgün mali boyut değerlerini korur ve bunları birikmiş kar hesabı için açılış bakiyelerini oluşturmak için kullanır. Ayrı kalan gelir açılış bakiyeleri daha sonra her bir benzersiz mali boyut değer birleşimleri için oluşturulur. **Birini kapat** seçiliyse, bu mali boyut ile nakledilmiş olan tüm hareketler, **Birini kapat** içerisinde girilmiş olan başlangıç bakiyesinde kalan gelir başlangıç bakiyesinde özetlenir. Örneğin, mali yıl için tüm hareketlerin **Ana hesap - Departman** hesap yapısıyla nakledilmiş olduğunu varsayalım. Şablondaki **Departman** mali boyutu için **Birini kapat** seçilir ve boyut değeri olarak **100** girilir. Departmanlar 200, 300 ve 400'e nakledilen tüm hareketleri toplam geliri 100.000$ ise, **Birikmiş kar - 100** için bir açılış bakiyesi oluşturulacaktır. **Birini kapat**'ı seçerseniz fakat mali boyut değerini boş bırakırsanız tüm hareketler bu boyut değeri boş olarak kalan gelirlere nakledilir.

## <a name="run-the-year-end-close-process"></a>Yıl sonu kapanış işlemini çalıştırın

Yıl sonu kapanış şablonları oluşturulduktan sonra, yıl sonu kapanışı işlemini **Yıl sonu kapanışı** sayfasında (**Genel muhasebe \> Dönem kapanışı \> Yıl sonu kapanışı**) başlatabilirsiniz. Yıl sonu kapanışını çalıştırmadan önce, şablonların kurulum sayfasını açmak için **Yıl sonu kapanış şablonu kurulumu**'nu seçerek yeni yıl sonu kapanış şablonları ekleyebilir veya var olan şablonları değiştirebilirsiniz.

Yıl sonu kapanış şablonunu seçin ve sonra Eylem Bölmesi'nde **Yıl sonu kapanışını çalıştır**'ı seçin. Yıl sonunu kapattığında çalıştırdığınız şablondan tüm tüzel kişilikleri veya tüzel kişiliklerin bir alt kümesini seçin. Bir mali yıl içinde ilk kez yıl sonu kapanışı çalıştırıyorsanız tümü için başlangıç bakiyeleri oluşturmak üzere tüm tüzel kişilikleri seçin. Yıl sonu kapanışını daha önce çalıştırdıysanız yalnızca düzeltme girişlerinin deftere nakledildiği tüzel kişilikler için yeniden çalıştırmak isteyebilirsiniz.

Ardından, yıl sonu kapatma işleminin çalıştırılacağı mali yılı seçin. Mali yılın son dönemi için birden fazla kapanış dönemi varsa **Dönem adı** alanı kullanılabilir duruma gelir. Kurulum kapanış hareketini oluşturmak üzere tanımlanmışsa kapanış hareketini deftere nakletmek için kullanılacak kapanış dönemini seçebilirsiniz.

Ardından, bir makbuz numarası girin. Aynı fiş numarası, yıl sonu kapanış işlemi için seçilen tüm tüzel varlıklar için kullanılır. Makbuz numarası bir numara serisi kullanılarak oluşturulmaz.

Varsayılan olarak yıl sonu kapatma işlemi toplu iş modunda çalışır. Bu nedenle, başlattıktan sonra diğer etkinliklere dönebilirsiniz.

Hesap yapıları mali yıl boyunca değişebileceğinden, ilgili hesap yapısı her zaman tanımlanamaz. Bu nedenle, yıl sonu kapatma işlemi hesap yapılarına uymaz. Açılış hareketleri oluşturulduğunda, bakiyeler yıl sonu kapanış şablonunda tanımlanmış olan mali boyutlarla ileri aktarılır. Açılış bakiyeleri girişi, geçerli hesap yapısında bulunmayan mali boyutları ve geçerli hesap yapısında geçerli olmayan bölüm kombinasyonlarını içerebilir. Kuruluşunuz birikmiş karlar başlangıç bakiyesi için bir mali boyutu dışarıda bırakmak istiyorsa, mali boyutu **Birini kapat** olarak ayarlayın ve boyut değerini boş bırakın.

İşlem tamamlandıktan sonra, bir tüzel kişilik ve mali yılın her kombinasyonu için bir kayıt oluşturulur. Yalnızca erişiminiz olan tüzel kişilikler için olan kayıtları görürsünüz. Her kayıt, işlemin çalıştırıldığı sistem tarih ve saatini ve yıl sonu kapanışı için oluşturulan fişlere doğrudan bir bağlantı içerir.

[![Yıl sonu kapanış sayfasının Yıl sonu kapanış geçmişi hızlı sekmesinde oluşturulan kayıtlar](./media/run-yr-end-close.png)](./media/run-yr-end-close.png)

Yıl sonu kapanışını yeniden çalıştırırsanız **Genel muhasebe parametreleri** sayfasındaki **Yılı yeniden kapatırken var olan yıl sonu girişlerini sil** seçeneğinin ayarına bağlı olarak tüzel kişilik ve mali yılın her kombinasyonu için bir veya birden çok kayıt görürsünüz:

- Seçenek **Evet** olarak ayarlanırsa önceki yıl sonu kapanışı için fiş silinir. Kayıt **Ters** olarak işaretlenir ve tersine çevirme işleminin yapıldığı tarih ve saat damgası eklenir. Ayrıca, makbuz numarası bağlantısı kaldırılır. Yıl sonu kapanışı tamamlandığında, oluşturulan yeni fiş için yeni bir kayıt oluşturulur.
- Seçenek **Hayır** olarak ayarlanırsa önceki yıl sonu kapanışı için kayıt fiş bağlantısıyla birlikte kalır. Yıl sonu kapanışı her yeniden çalıştırılmasında, yeni fişlere bir bağlantıyla birlikte yeni bir kayıt oluşturulur.

## <a name="reverse-the-year-end-close-process"></a>Yıl sonu kapanış işlemini tersine çevirme

**Yıl sonu kapanışı** sayfasında, yıl sonu kapanışını tersine çevirebilirsiniz. Tüzel kişilik ve tersine çevrilmesi gereken mali yıl kombinasyonu kaydını seçin ve sonra **Yıl sonu kapanışını tersine çevir**'i seçin. Tersine çevirme işlemi, mali yıl için oluşturulan tüm açılış ve kapanış fişlerini siler. Kayıt **Ters** olarak işaretlenir ve tersine çevirme işleminin yapıldığı tarih ve saat damgası eklenir. Ayrıca, makbuz numarası bağlantısı kaldırılır. Yıl sonu kapatma işlemi gibi, tersine çevirme işlemi de toplu iş modunda çalışır.

Kılavuzun üzerinde kullanılabilen **Tersine çevrilenleri göster** onay kutusu, tersine çevrilen yıl sonu kapanışı işlemlerinin kayıtlarını gizlemenizi veya göstermenizi sağlar. **Yıl sonu kapatmayı tersine çevir** işlemini çalıştırdıktan sonra, kaydı görmek için **Tersine çevrilenleri göster** onay kutusunu seçmeniz gerekebilir. Diğer bilgileri görüntülemek için ek filtreler ayarlayabilirsiniz.

[![Yıl sonu kapanışı sayfasında ters çevrilen yıl sonu kapanışı işlemlerinin kayıtlarını görmek için Tersine çevirlenleri göster onay kutusunu kullanma](./media/rvrs-yr-end-close.png)](./media/rvrs-yr-end-close.png)

Daha fazla bilgi için bkz. [Genel muhasebe defterini dönem sonunda kapatmak](close-general-ledger-at-period-end.md) ve [Mali yılı kapatmak](tasks/close-fiscal-year.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
