---
title: Yıl sonu kapanışı
description: Bu başlık, genel muhasebe yıl sonu kapatma işlemini çalıştırmak için gerekli kurulum ve adımları açıklar.
author: kweekley
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3071365640eb6c012cb9af5461e885bb3f135143
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846185"
---
# <a name="year-end-close"></a>Yıl sonu kapanışı

[!include [banner](../includes/banner.md)]

Bu başlık, genel muhasebe yıl sonu kapatma işlemini çalıştırmak için gerekli kurulum ve adımları açıklar. 

Bir mali dönem sonunda, açılış bakiyelerini yeni yıla aktarmak için yıl sonu kapanış sürecini yürütmeniz gerekir. Çoğu kuruluş yıl sonu kapatma işlemini birden çok kez yürütür. İlk kez, bakiyeleri yeni mali yıla aktarmak olacaktır. Bu yıl sonu kapatma daha sonra yeniden çalıştırılabilir, gerek duyduğu kadar, bakiyeleri ayarlanmış girişlerden yeni mali yıla taşımak için. 

Yıl sonu kapatma işlemi sırasında, olası hareketlerin iki türü oluşturulur. Bir Açılış hareketi her zaman oluşturulur ve açılış bakiyesini yeni mali yılda oluşturmak için kullanılır. Açılış hareketi, bilanço genel muhasebe hesap defteri bakiyelerini yeni mali yılda gösterir ve kar ve zarar genel muhasebe defteri bakiyelerini kalan gelirler genel muhasebe defteri hesabında yeni mali yılda dengeler. Kapanış hareketi, kapatılan mali yıldaki kar ve zarar hesaplarının bakiyesini sıfıra indirmek için isteğe bağlı oluşturulur.

## <a name="prepare-to-run-the-year-end-close"></a>Yıl sonu kapamayı çalıştırmaya hazırlamak
Yıl sonu kapanış işlemini çalıştırmadan önce, aşağıdakiler için ayarları doğrulayın: 

**Ana hesap** sayfasında:

-   **Ana hesap türü** nün her ana hesap için doğru tanımlandığını doğrulayın. Ana hesap türü, ana hesabın bakiyesinin bir açılış bakiyesi olarak mı yoksa kapalı olarak mı kalan gelirlere Açılış hareketinde ileri taşınacağı belirlemek için kullanılır.
-   **Açılış hesabı** alanı, ana hesabın bakiyesinin yıl sonu kapama sırasında yeni bir hesaba aktarılması için kullanılabilir. Yeni ana hesap, **Açılış hesabı** alanına girilir. Genellikle bu, bilanço ana hesapları için, ana hesap devre dışı bırakıldığında ve yeni bir ana hesap, yeni mali yıl için kullanıldığında kullanılacaktır.

**Genel muhasebe parametreleri** sayfasında **Mali yıl kapanışı** altında:

-   **Yıl sonu hareketlerini silerek kapa** seçeneği, sistem tarafından oluşturulan önceki yıl kapanışının Açılış hareketinin, yıl sonu kapanışı tekrar çalıştırıldığında silinip silinmeyeceğini belirtmek için kullanılır. Bu seçenek **Evet** olarak ayarlanırsa, önceki Açılış hareketi silinir ve yeni bir Açılış hareketi geçerli bakiyelere göre oluşturulur. Bu seçenek **Hayır** olarak ayarlanırsa, önceki Açılış hareketi kalır ve ek bir Açılış hareketi, bakiyeleri ileriye doğru, önceki yıl kapanışı hareketlerinden ileriye doğru ayarlamak için oluşturulur.
-   **Aktarma sırasında kapanış hareketlerinin oluşturması** seçeneği, kar ve zarar hesaplarına ait bakiyeler arasında sıfır durumuna getirmek için kapatılan mali yılın kapanış hareketlerini oluşturması için kullanılır. Bu seçenek **Evet** olarak ayarlanırsa, hem Açılış hareketi hem de Kapanış hareketi oluşturulur. Bu seçenek **Hayır** olarak ayarlanırsa, yalnızca Açılış hareketi bir sonraki mali yılda, bakiyeleri aktarmak için oluşturulur. Kar ve zarar hesabı bakiyelerini, mali yılın sonunda kalır.
-   **Mali yıl durumunu kalıcı kapalı olarak ayarlama** seçeneği, mali yılı kalıcı olarak kapalı duruma ayarlamak için kullanılır. Bu ayarı dikkatle kullanın çünkü kalıcı olarak kapalı tüm dönemlerin durumu, önceki mali yıla ayarlama yapmayı engellemek için yeniden açılamaz. En iyi uygulama bunu **Hayır** olarak ayarlamaktır.
-   **Fiş numarası doldurulmalıdır** seçeneği, bir fiş numarasının yıl sonu kapatma işlemi çalıştırırken gerekip gerekmediğini tanımlamak için kullanılır. Açılış hareketini kolayca tanımlamak için en iyi uygulama, bir fiş numarasını zorunlu kılmaktır.

**Mali takvim** sayfası üzerinde:

-   Yıl sonu kapanışını çalıştırmadan önce bir sonraki mali mevcut olmalıdır. Sonraki mali yıl, açılış döneminde açılış bakiyelerini oluşturmak için gereklidir.

**Genel muhasebe takvimi** sayfasında:

-   İsteğe bağlı: Yeni hareketlerin girilmesini önlemek için kapatılan mali için her mali dönem **Tutulan** olarak ayarlanabilir. Ayarlama girdileri tanımlandıktan sonra, ayarlama girişleri göndermek için tutulan dönemler yeniden açılabilir, yıl sonu kapanış işlemi çalıştırılmış olsa bile.

## <a name="define-year-end-close-templates"></a>Yıl sonu kapanış şablonlarını tanımlama
Sistem yapılandırıldıktan sonra, yıl sonu kapanış işlemi çalıştırılabilir. **Yıl sonu kapanış** sayfası üzerinde, yıl sonu kapanışının çalıştırılacağı tüzel varlıklar grubu için bir şablon tanımlanabilir. Bu şablon, her yıl sonu kapanışında yeniden kullanılır ancak kuruluşunuz değişim gösterirse değiştirilebilir. 

Öncelikle, şablon için **Grup adı** belirleyin ve mali takvimi seçin. Grup adı, tüzel varlıkların dahil olduğu grubu tanımlamalıdır.  Örneğin şablonlar, Kuzey Amerika tüzel varlıkları, EMEA tüzel varlıkları ve APAC tüzel varlıkları için ayrı gruplar ile coğrafyaya dayanarak ayarlanabilir. 

Ardından, tüzel varlıklar şablona eklenebilir. Tüzel varlıklar, bir kuruluş hiyerarşisi seçerek veya tüzel varlıkları seçerek eklenebilir. Bir kuruluş hiyerarşisi seçilirse, sadece bu hiyerarşi içerisindeki, bu seçili mali takvimi kullanan tüzel varlıklar şablona eklenecektir. Tüzel varlıkları şablona eklemek için kullanırsanız, sadece aynı mali takvimi kullanan tüzel varlıklar eklenebilir. Yıl sonu kapanışı, takvimden takvime farklılık gösterebilen bir mali yıl seçilerek çalıştırıldığı için aynı mali takvim kullanılabilir. 

Tüzel varlıklar eklendikten sonra, her bir tüzel varlık için kalan kazançlar ana hesaplarını tanımlayın. **Son yıl sonu kapanışın tarihi** alanı, tüzel kişilik için yıl sonu kapanışının her çalıştırıldığında güncelleştirilir. 

**Mali boyut** sekmesi, Açılış hareketinde kullanılacak mali boyutları tanımlamak için kullanılır. Tanımladığınız ayarların, sadece **Tüzel varlıklar** kılavuzunda seçmiş olduğunuz tüzel varlık için geçerli olduğunu unutmayın. Kılavuzdaki her tüzel varlık için kurulumu tekrar edeceksiniz. 

**Transfer bilanço boyutları**, bilançoya hesaplarına nakledilen hareketlerdeki finansal boyutların, Açılış hareketinde tutulup tutulmayacağını belirlemek için kullanılır. En iyi uygulama bunu **Evet** olarak ayarlamaktır. **Aktarıma kar ve zarar boyutları**, kar ve zarar hesaplarına nakledilmiş olan hangi finansal boyutların, kalan gelirler ana hesabına aktarılacağını belirlemek için kullanılır. Öncelikle, hangi finansal boyutların seçilen tüzel varlıkla ilişkili olduğunu tanımlayın. Bu, yıl boyunca nakledilmiş olan tüm mali boyutları dahil edecektir, finansal boyut aktif bir yapının parçası olmasa bile. Daha sonra, her bir boyutu **Kapalı tek** veya **Tümü kapalı** olarak tanımlayın.  Varsayılan **Tümü kapalı** olmaktadır, bu da orijinal mali boyut değerlerini nakledilmiş hareketlerden tutar ve onları kalan gelirler hesapları için açılış bakiyeleri oluşturmakta kullanır. Ayrı kalan gelir açılış bakiyeleri daha sonra her bir benzersiz mali boyut değer birleşimleri için oluşturulur. **Kapalı tek** seçiliyse, bu mali boyut ile nakledilmiş olan tüm hareketler, **Kapalı tek** içerisinde girilmiş olan başlangıç bakiyesinde kalan gelir başlangıç bakiyesinde özetlenir. Örneğin, mali yıl için tüm hareketlerin Ana hesap - Departman hesap yapısıyla nakledilmiş olduğunu varsayalım. Departman mali boyut üzerindeki şablonda, **Kapalı tek** seçilir ve 100 değeri girilmiştir. Departmanlar 200, 300 ve 400'e nakledilen tüm hareketleri toplam geliri 100.000$ ise, Kalan gelirler - 100 için bir açılış bakiyesi oluşturulacaktır. **Kapalı tek** seçerseniz ve mali boyut değerini boş bırakırsanız, tüm hareketler bu boyut değeri boş olarak kalan gelirlere nakledilir. 

Yıl sonu kapama işlemi hesap yapılarına uymaz. Bunun sebebi, hesap yapılarının mali yıl boyunca değişebilmesi ve her zaman ilgili hesap yapısını bu değişiklikler yüzünden tespit edilememesidir.  Açılış hareketleri oluşturulduğunda, bakiyeler yıl sonu kapanış şablonunda tanımlanmış olan mali boyutlarla ileri aktarılacaktır. Açılış bakiyeleri girişi, geçerli hesap yapısında bulunmayan mali boyutları ve geçerli hesap yapısında geçerli olmayan bölüm kombinasyonlarını içerebilir. Kuruluşunuz kalan gelirler başlangıç bakiyesi için bir mali boyutu dışarıda bırakmak istiyorsa, mali boyutu **Kapalı tek** olarak ayarlayın ve boyut değerini boş bırakın.

## <a name="run-the-year-end-close-process"></a>Yıl sonu kapanış işlemini çalıştırın
Yıl sonu kapanış şablonları oluşturulduktan sonra, yıl sonu kapanış işlemi **Yıl sonunu çalıştır** seçeneğini Eylem bölmesinde seçerek başlatılır. Yıl sonu kapanışını çalıştırmak için şablondan tüzel kişiliklerin tamamını ya da alt kümesini seçin. Yıl sonu kapanışı bir mali yılda ilk defa çalıştırılırken, çoğu tüzel varlık için yıl sonu bakiyeleri oluşturmak için tüm tüzel varlıkları kapatmanız olasıdır. Yıl sonu kapanışın yeniden çalıştırırsanız, bunu yalnızca ayarlanmış girişlerin nakledildiği tüzel varlıklar için çalıştırmayı tercih edebilirsiniz. 

Yıl sonu kapanış işlemini karşıt çalıştırmak istediğiniz mali yılı seçin. Mali yılın son dönemi için birden fazla kapanış dönemi mevcutsa, **Dönem adı** alanı kullanılabilir duruma gelir ve böylece siz hangi kapanış döneminin Kapanış hareketine nakledileceğini seçebilirsiniz, eğer kurulum Kapanış hareketini oluşturmak üzere tanımlandıysa. 

Bir fiş numarası girin, bu durum Genel muhasebe parametrelerine bağlı olarak gerekli olabilir veya olmayabilir. Aynı fiş numarası, yıl sonu kapanış işlemi için seçilen tüm tüzel varlıklar için kullanılır. Fiş numarası, bir sayı serisi kullanılarak oluşturulmaz. Gerekli olmasa bile bir fiş numarası girmek en iyi uygulamadır. Fiş numarası giymek, yeni mali yıldaki Açılış hareketini bulmayı kolaylaştırır. Bir fiş numarası girilmezse, fiş Açılış hareketi için boş olacaktır. 

Bir önceki yıl kapanışını seçilen yıl için tersine çevirmek isterseniz, **Önceki kapanışı geri al** seçeneğini **Evet** olarak ayarlayın. Yıl sonu kapanışı geri çevrilir, ancak işlem istenildiği zaman yeniden çalıştırılabilir. Yıl sonu kapanışı geri çevirirseniz, **Son yıl sonu kapanışı tarihi** kullanılamayacaktır. 

Yıl sonu kapanış işlemi, toplu iş modu varsayılanına döner. Kullanıcının diğer faaliyetlerine dönmesine izin vermek için işlemi toplu iş modunda çalıştırmak bir en iyi uygulamadır. Yıl sonu kapanış süreci tamamlandığında, **Son yıl sonu kapanışının tarihi**, oturum tarihi ile güncelleştirilecektir.

Daha fazla bilgi için bkz. [Genel muhasebe defterini dönem sonunda kapatmak](close-general-ledger-at-period-end.md) ve [Mali yılı kapatmak](tasks/close-fiscal-year.md).



