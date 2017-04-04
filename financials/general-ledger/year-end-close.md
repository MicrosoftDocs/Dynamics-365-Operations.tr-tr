---
title: "Yıl sonu kapanışı"
description: "Bu konuda gerekli Kurulum ve genel muhasebe yıl sonu kapatma işlemini çalıştırmak için gereken adımları açıklar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 22233cfa1df79076c8ea42f75ea309bac990d574
ms.lasthandoff: 03/31/2017


---

# <a name="year-end-close"></a>Yıl sonu kapanışı

Bu konuda gerekli Kurulum ve genel muhasebe yıl sonu kapatma işlemini çalıştırmak için gereken adımları açıklar. 

Mali yıl sonunda, yeni yıl için açılış bakiyelerini transfer etmesini yıl sonu kapatma işlemi çalıştırmanız gerekir. Çoğu kuruluş yıl sonu kapatma işlemi birden çok kez çalıştırmak. İlk kez yeni bir mali yıl içinde taşınan bakiyeleri almak için olacaktır. Yıl Sonu Kapanış sonra tekrar defalarca bakiyelerin girişler yeni mali yıl içinde ayarlaması taşımak için gerekli olduğu gibi çalıştırabilirsiniz. 

Kapatma işlemi sırasında yıl sonu, oluşturulan olası hareketlerinin iki türü vardır. Açılış hareketi her zaman oluşturulur ve yeni mali yıldaki açılış bakiyelerini oluşturmak için kullanılır. Açılış hareketi yeni mali yıldaki bilanço genel muhasebe hesap bakiyelerini gösterir ve kar ve zarar genel muhasebe hesap bakiyelerindeki Akçe genel muhasebe hesabı'ndan yeni mali yıldaki dengeler. Kapanış hareketleri Kapatılan Mali yılın sıfır kadar kar ve zarar hesaplarına ait bakiyeler arasında getirmek için isteğe bağlı olarak oluşturulur.

## <a name="prepare-to-run-the-year-end-close"></a>Yıl Sonu Kapanış çalıştırmak hazırlama
Yıl sonu kapatma işlemi çalıştırmadan önce aşağıdaki ayarları doğrulayın: 

**Ana hesap** sayfasında:

-   Doğrulamak **ana hesap türü** ana her hesap için doğru olarak tanımlanır. Ana hesap türü, ana hesap bakiyesini Açılış bakiyesi olarak ileri veya kapalı karı içine açılış hareket güncelleştirilecektir olup olmadığını belirlemek için kullanılır.
-   **Hesap açma** alanına ana hesap bakiyesini kapatın yıl sonu sırasında yeni bir ana hesap aktarmak için kullanılabilir. Yeni ana hesap girildiğini **hesap açma** alan. Genellikle bu ana bilanço hesapları için ana hesap devre dışı bırakılan ve yeni bir ana hesap yeni mali yıl için kullanıldığında kullanılacaktır.

Üzerinde **genel muhasebe parametreleri** altında sayfa **mali yıl kapanışı**:

-   **Sil yıl hareketlerini kapat** seçeneği, yıl sonu kapanış yeniden çalıştırdığınızda, sistem tarafından oluşturulan açılış hareketten alınan bir önceki yıl sonu kapanış silinip silinmeyeceğini belirtmek için kullanılır. Bu seçenek ayarlanırsa **Evet**, önceki açılış hareketi silinir ve yeni bir açılış hareket geçerli bakiyelere göre oluşturulur. Bu seçenek ayarlanırsa **No**, önceki açılış hareketi kalır ve önceki yıl sonu kapattıktan sonra deftere nakledilen hareketler ayarlaması bakiyeleri ileri taşımak için ek bir açılış hareketi oluşturulur.
-   **Aktarma sırasında kapanış hareketleri oluşturması** seçeneği, kar ve zarar hesaplarına ait bakiyeler arasında sıfıra duruma getirmek için kapatılan mali yılın kapanış hareketleri oluşturması için kullanılır. Bu seçenek ayarlanırsa **Evet**, hareket açılış ve kapanış hareketi oluşturulur. Bu seçenek ayarlanırsa **No**, bakiyelerini transfer etmesini sonraki mali yıl açılış hareketi oluşturulur. Kar ve zarar hesabı bakiyelerini, mali yılın sonunda kalır.
-   **Ayarlanmış mali yıl durum tamamen kapalı** seçenek mali yıl kalıcı olarak kapalı durumuna ayarlamak için kullanılır. Mali yılda deftere nakledildi gelen ayarlamaları önleme tamamen kapalı durumundaki tüm dönemler açılamaz çünkü dikkatli olun, bu ayarı kullanın. Bunu ayarlamak için en iyi yöntem olduğu **No**.
-   **Fiş numarası doldurulmalıdır** seçeneği bir fiş numarası yıl sonu kapatma işlemi çalıştırırken gerekip gerekmediğini tanımlamak için kullanılır. Kolayca açılış hareketi tanımlamak için bir fiş numarası istemek için iyi bir uygulamadır.

Üzerinde **mali takvim** sayfa:

-   Bir sonraki mali yılın yıl sonu kapanış çalıştırmadan önce varolmalıdır. Sonraki mali yılın açılış dönemi içinde başlayan bakiyeleri oluşturmak için gereklidir.

Üzerinde **defter Takvim** sayfa:

-   İsteğe bağlı: Her mali dönem için kapatılan mali yılın ayarlanabilir **tutulan** yeni hareketlerin girilmesini önlemek için. Ayarlama girdileri belirlenen zaman yıl sonu kapatma işlemi zaten çalıştırıyor olsa açık tutma dönemleri ayarlama girişlerini deftere nakletmek için yeniden açılabilir.

## <a name="define-year-end-close-templates"></a>Yıl sonu kapatma şablonları tanımlama
Sistemi yapılandırdıktan sonra yıl sonu kapatma işlemi çalıştırabilirsiniz. Üzerinde **yıl sonu Kapat** sayfası, Grup tüzel yıl sonu kapatma işlemini çalıştırmak için bir şablon tanımlanabilir. Şablonu Kapat her yıl sonu yeniden, ancak kuruluşunuz değiştiğinde değiştirilebilir. 

İlk olarak tanımlayan **grup adı** için şablon ve mali takvimi seçin. Grup adı, Grup dahil tüzel tanımlamalıdır.  Örneğin, şablonlar Coğrafya üzerinde Kuzey Amerika tüzel kişilikler, Orta Doğu ve Afrika tüzel kişilikler ve APAC tüzel kişilikler için oluşturulan ayrı gruplar ile göre ayarlanabilir. 

Ardından, tüzel kişilikler şablonuna eklenebilir. Tüzel bir organizasyon hiyerarşisine seçerek veya tüzel seçip eklenebilir. Bir organizasyon hiyerarşisine seçtiyseniz, seçili mali takvimi kullanan tüzel kişilikler hiyerari içindeki şablona eklenir. Tüzel kişilikler için şablon eklemek için kullanırsanız, yalnızca aynı mali takvimle tüzel kişilikler eklenebilir. Aynı mali takvimi, Takvim Takvim değişebilir bir mali yıl, seçerek yıl sonu yakın çalıştığı için gereklidir. 

Tüzel kişilikler eklendikten sonra her bir tüzel kişilik yedek akçe ana hesaplar tanımlayın. **Geçen yıl bitiş tarihi Kapat** yıl sonu yakın her çalıştırdığınızda bir tüzel kişilik için alan güncelleştirilir. 

**Mali boyut** sekmesini mali boyutları açılış hareket için kullanılacak tanımlamak için kullanılır. Olduğunu tanımlama ayarları yalnızca seçilen tüzel kişilik ilgili olduğuna dikkat edin **tüzel** kılavuz. Kur, kılavuzdaki her tüzel kişilik için yinelenir. 

**Transfer Bilanço boyutları** bilanço hesaplarına nakledilen hareketler üzerindeki mali boyutları açılış hareketi üzerinde tutulan olduğunu tanımlamak için kullanılır. Bu seçeneği belirlemek en iyi yöntemdir **Evet**. **Transfer kar ve zarar boyutları** Akçe ana hesap hangi mali boyutları hareket nakledilen kar ve zarar hesabına aktarılır tanımlamak için kullanılır. Öncelikle, yasal varlıkla ilgili mali boyutları tanımlayın. Mali boyut etkin firma yapısının parçası olmasa bile bu karşı yıl boyunca, deftere nakledilen tüm mali boyutları içerir. Ardından, her boyut olarak tanımlamak **Kapat tek** veya **Tümünü Kapat**.  Varsayılan değer **Tümünü Kapat**, hangi orijinal mali boyut tutan değerleri deftere nakledilen hareketleri ve yedek akçe hesabı oluşturma Açılış bakiyeleri için bunları kullanır. Başlangıç bakiyelerini ayrı Akçe benzersiz her mali boyut değerleri birleşimi için oluşturulur. Yoksa **Kapat tek** olan seçili, o ile mali boyut deftere nakledilen tüm hareketleri Başlangıç Bakiyesi alanından sonra girdiğiniz boyut değeri için bir yedek akçe içine özetlenir **Kapat tek**. Örneğin, tüm hareketler için mali yıl ana hesap - departman hesabı yapısıyla deftere nakledilen varsayalım. Şablonu Bölümü mali boyut üzerinde **Kapat tek** seçilir ve girilen değer 100'dür. $100,000 200, 300 ve 400 Departmanlar için deftere nakledilen tüm hareketlerin toplam gelir ise, bir açılış bakiyesi Retained yedek akçe - 100 oluşturulur. Seçerseniz **Kapat tek** ve Finans boyut değerini boş bırakın, tüm hareketleri için yedek akçe boş olan bu boyut değeri deftere nakleder. 

Yıl sonu kapatma işlemi hesap yapılarına uymayan. Bu mali yıl hesap yapıları değiştirebilir ve her zaman ilgili hesap yapısı nedeniyle bu değişiklikleri belirlemek mümkün değildir çünkü.  Açılış hareketleri oluşturulurken bakiyeleri İleri mali boyutları ile yıl sonu kapatma şablonda tanımlanan şekilde güncelleştirilecektir. Başlangıç bakiyelerin girişler mali boyutları artık artık geçerli hesap yapısı içinde geçerli Cari hesap yapısı ve segment birleşimlerini içerebilir. Kuruluşunuzun tutulan getirisi Başlangıç bakiyesi, mali boyut ayarlamak için mali boyut dışlanacak istiyorsa, **Kapat tek** ve boyut değerini boş bırakın.

## <a name="run-the-year-end-close-process"></a>Yıl sonu kapatma işlemini çalıştırın.
Yıl sonu kapatma şablonları oluşturulduktan sonra yıl sonu kapatma işlemi seçerek başlatılır **mali yıl** eylem bölmesi. Tümünü Seç veya bir alt kümesi için yıl sonu kapanış çalıştırılacak şablondan tüzel kişilikler. Yıl sonu çalışan kapattığınızda bir mali yıldaki ilk kez, büyük olasılıkla tüm tüzel kişilikler için Başlangıç bakiyelerini oluşturmak için tüm tüzel kişilikler seçecektir. Yıl Sonu Kapanış yeniden çalıştırıyorsanız, işlem yalnızca kendisi için ayarlama girişlerinin deftere nakledildiği tüzel kişilikler için çalıştırmayı seçebilirsiniz. 

Yıl sonu Kapat uygulamalarına karşı çalıştırmak istediğiniz mali yılı seçin. Birden fazla kapanış dönemi için mali yılın son döneminden varsa **dönem adı** kapanış hareketi oluşturmak için ayarı tanımlıysa kapanış hareketi nakletmek için hangi kapanış dönemi seçebilmeniz için alan kullanılabilir olacak. 

Girin bir fiş numarası, hangi veya, Kur'un genel muhasebe parametreleri bağlı olarak, gerekli olmayabilir. Yıl sonu kapatma işlem için seçilen tüzel kişilikler için aynı fiş numarası kullanılır. Fiş numarası, numara serisini kullanan oluşturulmaz. Gerekli değildir olsa bile bir fiş numarasını girmek için iyi bir uygulamadır. Fiş numarası girerek yeni mali yıldaki açılış hareketi bulmayı kolaylaştırır. Fiş numarası olmayan girdiyseniz, fiş için açılış hareketi boş olacaktır. 

Bir önceki yıl sonu kapanışı seçili mali yıl için tersine çevirmek isterseniz, set **yakın önceki geri** için **Evet**. Yıl Sonu Kapanış tersine, ancak işlemin herhangi bir zamanda yeniden çalıştırabilirsiniz. Yıl sonu kapatma, ters **geçen yıl bitiş tarihi Kapat** kullanılamayacak. 

Toplu iş modunda çalıştırmak için yıl sonu kapatma işlemi Varsayılanları. Toplu iş modunda, diğer etkinlikler için dönmek kullanıcı izin vermek için işlemi çalıştırmak için iyi bir uygulamadır. Yıl sonu kapatma işlemi tamamlandıktan sonra **geçen yıl bitiş tarihi Kapat** oturum tarihle güncelleştirilir.

Daha fazla bilgi için bkz: [dönem sonu genel muhasebede Kapat](close-general-ledger-at-period-end.md).


