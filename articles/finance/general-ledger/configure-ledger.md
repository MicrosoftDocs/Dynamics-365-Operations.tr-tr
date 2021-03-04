---
title: Genel muhasebe defterlerini yapılandırma
description: Bu konuda, her tüzel kişilik için genel muhasebe defterlerinin nasıl yapılandırılacağı hakkında bilgi sağlanmaktadır. Her tüzel kişiyle kullanılacak para birimlerinin, mali takvimlerin, hesap planlarının ve hesap yapılarının nasıl seçileceği hakkında bilgiler sunulur.
author: kweekley
manager: ''
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Ledger
audience: Application User
ms.reviewer: roschlom
ms.search.scope: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-09
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 929ab7ae66a217de836ce49373faed76325c4d3a
ms.sourcegitcommit: ac0a676c91e3053ad7f9432d576c9af3ff98a99a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4449031"
---
# <a name="configure-ledgers"></a>Genel muhasebe defterlerini yapılandırma

[!include [banner](../includes/banner.md)]

Bu konuda, her tüzel kişilik için genel muhasebe defterlerinin nasıl yapılandırılacağı hakkında bilgi sağlanmaktadır. Her tüzel kişiyle kullanılacak para birimlerinin, mali takvimlerin, hesap planlarının ve hesap yapılarının nasıl seçileceği hakkında bilgiler sunulur.

## <a name="selecting-the-chart-of-accounts"></a>Hesap planını seçme

Microsoft Dynamics 365 Finance'teki her tüzel kişilik için genel muhasebe defteri hakkındaki ayrıntılar yapılandırılmalıdır. **Genel muhasebe** sayfasında seçili tüzel kişilik için kullanılacak hesap planını ve hesap yapılarını seçebilirsiniz. Aynı hesap planını ve hesap yapılarını kullanmak için her tüzel kişilikteki **Genel muhasebe** sayfasını yapılandırarak hesap planınızı ve hesap yapılarınızı paylaşabilirsiniz. Ayrıca, her tüzel kişilikte yapılandırmaların bir kısmını paylaşabilir ve her tüzel kişilikte özel yapılandırmalara sahip olabilirsiniz.

Tüzel kişiliklerinizin farklı hesap planları veya farklı hesap yapıları olması gerekiyorsa tüzel kişilik geçersiz kılma özelliği kullanışlı olabilir. Birden fazla tüzel kişilik için aynı hesap planını ve hesap yapılarını kullanıp tüzel kişilikleri geçersiz kılma özelliğiyle özel durumları yöneterek zaman içinde bakım işlemlerini kolaylaştırabilirsiniz.

Bir tüzel kişilik için hesap planı yapılandırmak amacıyla **Genel muhasebe \> Genel muhasebe kurulumu \> Genel muhasebe** bölümüne gidin. **Genel muhasebe** sayfasında **Hesap planı**'nı seçin ve ardından listeden kullanılacak hesap planını seçin. Bir değer seçtikten ve tüzel kişilikte hareketleri deftere naklettikten sonra hesap planının değiştirilemeyeceğini unutmayın.

Hesap planını ve ana hesapları planlama ve yapılandırma hakkında daha fazla bilgi için bkz. [Hesap planını planlama](plan-chart-of-accounts.md).

## <a name="selecting-account-structures"></a>Hesap yapılarını seçme

Dynamics 365 Finance'te her tüzel kişilik bir veya daha fazla hesap yapısını kullanacak şekilde yapılandırılabilir. Her hesap yapısı mali boyutları ve ana firmaların ve mali boyutların birleşimlerini tanımlar; bunlara hareketler deftere nakledilirken izin verilir. Aynı hesap yapılarını birden fazla tüzel kişilikte kullanabilirsiniz.

Birden fazla hesap yapınız varsa yalnızca ana firmaların ve mali boyutların örtüşen birleşimlerine sahip olmayan hesap yapılarını seçebilirsiniz. Örneğin, hesap yapılarınızdan birinin 1000 ile 1999 arasındaki ana hesaplar için iş birimi ekleyecek şekilde yapılandırıldığını düşünelim. Başka bir hesap yapısında, 1 ile başlayan ana hesaplar için bir Departman mali boyutu eklediniz. Bu durumda, hesap yapılarından yalnızca biri aynı tüzel kişiliğe eklenebilir.

Genel muhasebe defterinizin hesap yapılarını yapılandırmak için **Genel muhasebe** sayfasındaki **Hesap yapıları** hızlı sekmesinde **Ekle**'yi seçin, listeden bir hesap yapısı seçin ve ardından **Seç**'i belirleyin. Hesap yapılarının eklenmesi ve kaydedilmesi birkaç dakika sürebilir. Seçtiğiniz hesap yapılarının etkin olması gerektiğini unutmayın. Aksi takdirde, hesap yapılarının ayrıntıları bağlı oldukları tüzel kişiliklerde etkili olmayacaktır.

Hesap yapısını kaldırmak için **Genel muhasebe** sayfasındaki **Hesap yapıları** hızlı sekmesinde **Kaldır**'ı seçin. Genel muhasebenizden bir hesap yapısını kaldırırsanız bu hesap yapısının yapılandırması kullanılarak deftere nakledilen hareketleri kaldırmazsınız.

Hesap yapılarınızı ayarlama hakkında daha fazla bilgi için bkz. [Hesap yapılarını yapılandırma](configure-account-structures.md).

## <a name="configuring-calendars-for-the-ledger"></a>Genel muhasebe için takvimleri yapılandırma

Genel muhasebenin başka bir bileşeni de mali takvimdir. Her tüzel kişilik için bir mali takvim seçilmelidir. Aynı mali takvimi birden fazla tüzel kişilikte kullanabilirsiniz. Genel muhasebe için bir mali takvim seçtiğinizde takvimin bir kopyası oluşturulur. Bu kopyaya genel muhasebe takvimi adı verilir. Genel muhasebe takviminde dönemlerin durumunu ve her dönemdeki modülleri seçebilirsiniz.

Seçili tüzel kişiliğin takvimine erişmek ve takvimi güncelleştirmek için **Genel muhasebe** sayfasındaki Eylem Bölmesinde **Genel muhasebe takvimi**'ni seçin.

Takvimi seçmek için **Mali takvimler**'i seçin ve ardından listeden takvimi seçin. Hareketler tüzel kişilikte deftere nakledildikten sonra mali takvimi değiştirirseniz **Genel muhasebe dönemlerini yeniden hesapla** seçeneğini belirlemeniz gerekir. Ardından görüntülenen iletişim kutusunda, takviminizdeki dönemler için genel muhasebe bakiyelerini güncelleştirebilirsiniz. **Genel muhasebe dönemlerini yeniden hesapla** işlemini **Toplu iş** modunda çalıştırmanızı ve bu işi sisteminizde kritik olmayan işlemlerin yapıldığı bir zamanda çalıştırmanızı öneririz. Hareket sayısına ve mali boyut birleşimlerine bağlı olarak bu işlem biraz zaman alabilir.

Bir tüzel kişilik için mali takvim seçilmemişse söz konusu tüzel kişilikte bir hareketi deftere nakletmeyi denediğinizde hata iletisi alırsınız.

Daha fazla bilgi için bkz. [Mali takvimler, mali yıllar ve dönemler](../budgeting/fiscal-calendars-fiscal-years-periods.md).

## <a name="using-a-balancing-financial-dimension"></a>Dengeleme mali boyutu kullanma

Hesap planını seçtikten ve bir veya daha fazla hesap yapısı ekledikten sonra, isteğe bağlı olarak dengeleme mali boyutu olarak kullanılmak üzere tek bir mali boyut seçebilirsiniz. Seçtiğiniz boyut tüm hesap yapılarında mevcut olmalıdır. Ayrıca, tüm muhasebe girişlerinde dengelenmiş olmalıdır. Diğer bir ifadeyle, ana hesap ve dengeleme mali boyutu için borçlar ve alacaklar eşit olmalıdır. Sistem, **Otomatik hareketler için hesaplar** sayfasındaki **Birimlerarası - alacak** ve **Birimlerarası - borç** alanlarında belirtilen ana hesaplara göre girişleri dengelemek için otomatik olarak hareketler oluşturur.

Dengeleme girişleri hakkında daha fazla bilgi için bkz. [Birimlerarası muhasebe için dengelenmiş günlükler](example-balanced-journals-interunit-accounting.md).

## <a name="configuring-currencies-for-the-ledger"></a>Genel muhasebe için para birimlerini yapılandırma

**Genel muhasebe** sayfası, hareketler genel muhasebe defterine nakledilirken kullanılacak para birimlerini kontrol etmek ve tanımlamak için de kullanılır. Tüm fişlerdeki genel muhasebede **Muhasebe para birimi** sütununda kullanılan para birimi olan muhasebe para birimini belirtmeniz gerekir. Ayrıca, **Raporlama para birimi** sütununda isteğe bağlı olarak ikinci bir para birimi seçebilirsiniz. Bir raporlama para birimi seçerseniz, hareketler tüm fişlerde genel muhasebede yer alan **Raporlama birimi** sütununda bu para birimiyle kaydedilir.

Hareketler farklı bir para birimiyle deftere nakledilmişse sistem, otomatik olarak fişte hareket tutarını hareket para biriminden muhasebe para birimine ve raporlama para birimine çevirir. **Genel muhasebe** sayfasındaki **Muhasebe para birimi döviz kuru türü** alanında, fişte değerleri hareket para biriminden muhasebe para birimine dönüştürmek için kullanılması gereken döviz kurları için yapılandırılan döviz kuru türünü seçin. Bir raporlama para birimi seçtiyseniz, fişte değerleri hareket para biriminden raporlama para birimine dönüştürmek için kullanılması gereken döviz kurunu belirtmek üzere **Raporlama para birimi döviz kuru türü** alanını da ayarlamanız gerekir.

Bütçeleme işlevi kullanıyorsanız bütçe hareketlerini bir para biriminden diğerine dönüştürmek için kullanılacak döviz kurunu belirtmek için **Bütçe döviz kuru türü** alanını da ayarlayabilirsiniz.

İki para birimi kullanıyorsanız veya tek bir para birimini kullanıyorsanız ancak hareketler farklı bir para biriminde deftere naklediliyorsa **Genel muhasebe** sayfasındaki **Para birimi yeniden değerleme için hesaplar** hızlı sekmesini yapılandırmanız gerekir. Bu hızlı sekmede, **Para birimi yeniden değerleme hesapları** sayfasında hesap belirtilmemişse, hareketler deftere nakledilirken varsayılan olarak kullanılacak olan varsayılan gerçekleşmiş ve gerçekleşmemiş kazanç ve kayıp hesaplarını tanımlarsınız. (**Para birimi yeniden değerleme hesapları** sayfası, her para birimi için gerçekleşmiş ve gerçekleşmemiş kazançlar ve kayıplar için farklı hesaplar yapılandırmak amacıyla kullanılır.)

Gerçekleşmiş kazançlar ve kayıplar, tamamlanan hareketlerden elde edilen kar ve zararlardır. Kar ve zarar ekstresinde kaydedilirler. Gerçekleşmemiş kazançlar ve kayıplar, oluşan ancak hareketin tamamlanmadığı kar ve zararlardır. Diğer bir ifadeyle, bir faturayı deftere naklettiğiniz ancak faturanın henüz kapatılıp ödenmediği bir durum buna örnek oluşturabilir. Gerçekleşmemiş kazançlar ve zararlar bilançoya kaydedilir.

İki para biriminin nasıl kullanılacağı hakkında daha fazla bilgi için bkz. [Çift para birimi](dual-currency.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]