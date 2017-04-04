---
title: Kambiyo senedi Ayarla
description: "Bu konu, kambiyo ayarlama adımlarını açıklar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ce2142d946085d8bfc577accf1bb31a89ea29156
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bills-of-exchange"></a>Kambiyo senedi Ayarla

Bu konu, kambiyo ayarlama adımlarını açıklar.

Kambiyo senedi belirten başka bir şahıs, genellikle banka, şirket için belirtilen bir tutarı ödemesi gereken bir müşteriden gelen yazılı veya elektronik bir sıradır. Bir satış siparişi faturası veya serbest metin faturası için ödeme olarak kambiyo senedi kullandığınızda müşteri hesabını alacaklandırırsınız. Müşteri kambiyo senedini bankaya ödeyene kadar bu alacak tutarı kambiyo senedi tarafından teminat altına alınır. Genellikle, vade tarihinde kambiyo senedi faturayla kapatmayacağını. Bankanızdan kambiyo senedinin karşılığının ödendiğine ilişkin bir bildirim aldığınızda kambiyo senedini kapatabilirsiniz. Aşağıdaki durumlarda biri de, bankanız aracılığıyla bir kambiyo senedi çizebilirsiniz:

-   Vade tarihinde. Bu yaklaşım, tahsilat için havale olarak bilinir.
-   Vade tarihinden önce genellikle müşteri için ayarlanan ödeme koşulları formunda belirtilen iskonto tarihi. İskonto Tutarı, bir hareketi deftere naklettiğinizde bir gider hesabına nakledilir. Banka ödeme müşteriden alıncaya kadar kalan tutarı de borçtur. Bu yaklaşım, iskonto için havale olarak bilinir.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Kambiyo senetleri için deftere nakil profilleri ayarlama
Kullanmak **müşteri nakil profilleri** deftere nakil kambiyo senedi, protestolu kambiyo senedi, havaleler için toplama ve havaleler için indirim ile kullanabileceğiniz profilleri ayarlamak için sayfa. İçinde **hesap özeti** alan, özet hesabı için kambiyo senedi tutarlarını deftere nakletmek için seçin. Bu hesaba borç veya alacak, kambiyo senedi hareket türüne bağlı olarak:
-   Kambiyo senedi deftere nakledilir ve iskonto için havale veya tahsilat için havale nakledildiğinde alacak kambiyo senedi için bu hesaba borç kaydedilir.
-   Protestolu kambiyo senetlerinde, bu hesap protestolu bir kambiyo senedi nakledildiğinde borçlandırılır.
-   Tahsilat için havalelerde, bu hesap bir tahsilat için havale nakledildiğinde borçlandırılır.
-   İskonto için havalelerde, bu hesap bir iskonto için havale nakledildiğinde borçlandırılır.

İçinde **kapatma hesabı** alanında, nakit hesabı için kambiyo senedi tutarlarını deftere nakletmek için seçin. Hesap, bir kambiyo senedi kapatıldığında borçlandırılır. İçinde **satış vergisi ön ödemeleri** alan, ödemeler için kambiyo senedi kullanıldığında için satış vergisi tutarlarını deftere nakletmek için özet hesabı seçin. İçinde **iskonto hesabı pasifi** alanında, havaleler için iskonto iskonto tutarını deftere nakletmek için bir hesap seçin. Bu hesap, bir iskonto için havale deftere nakledildiğinde alacaklandırılır.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Kambiyo senedi Alacak hesapları parametrelerini hesaplarını ayarlama
Üzerinde **Accounts receivable parameters**, kambiyo senedi girilen deftere nakil profilleri varsayılan sayfa **muhasebe ve vergi** sekme. Numara serileri üzerinde tanımlanan **Number sequences** sekme.
Kambiyo senetleri için günlük adları ayarlama
------------------------------------------

Üzerinde **günlük adları** sayfasında, kambiyo senedi için kullanmak üzere en az beş günlük adları oluşturun. Günlük türleri şunlardır:
-   **Müşteri düzenlenen kambiyo senedi** – düzenlenen kambiyo senedi günlüğü için bir günlük adı oluşturun.
-   **Müşteri protestolu kambiyo senedi** -protestolu kambiyo senedi günlüğü için bir günlük adı oluşturun.
-   **Müşteri yeniden düzenlenen kambiyo senedi** – yeniden düzenlenen kambiyo senedi günlüğü için bir günlük adı oluşturun.
-   **Müşteri Banka havalesi** – havale günlüğü için bir günlük adı oluşturun.
-   **Müşteri ödenen kambiyo senedi** – ödenen kambiyo senedi günlüğü için bir günlük adı oluşturun.

Her kambiyo senedi günlüğü için günlük fişi sayfasında, kambiyo senedi hakkında bilgi girmek **kambiyo senedi** sekme. Kambiyo senedi günlüğü satırlarını deftere nakledildikten sonra üzerinde görebilmek için **kambiyo senedi günlüğü sorgu** sayfa ve **kambiyo senedi istatistikleri** sayfa.
Kambiyo senetleri için ödeme yöntemleri ayarlama
-----------------------------------------------

Üzerinde **ödeme yöntemleri** sayfa, kambiyo senedi için en az bir ödeme yöntemi ayarlamak. Birden fazla banka ile iş yapıyorsanız, kambiyo senedi gerektiren her banka havale biçimine karşılık gelen bir ödeme yöntemi ayarlamak.
Kambiyo senetleri için ödeme masrafları ayarlama
-----------------------------------------

Ödeme masrafı müşterilerden gelen ödemeleri toplama işlemi ile ilişkili bir şarj olur. Satırları olabilir birden fazla ödeme ücreti kurulumu her ödeme ücretiyle ilişkili. Kurulum satırları, ödeme masrafları için varsayılan tutarların nasıl hesaplandığını denetlemek için kullanabilirsiniz. Örneğin, ödeme, ödeme belirtimleri, para birimleri ve dönemleri yöntemleri için Kurulum satırları oluşturabilirsiniz. Kurulum satırları yüzdesi veya günün belirli aralıklarla dayalı tutar için de oluşturabilirsiniz. Örneğin, bir ödeme vadesi geçmiş zaman uzunluğuna bağlı bir vade farkı yüzdesini ayarlayabilirsiniz. Farklı havale türleri için farklı masraflar Banka gibi giderler **koleksiyonu** veya **indirim**, bir havale her türü için ayrı bir ödeme ücreti satır ayarlayın.
Banka havale dosyaları için havale ücretleri ayarlama
------------------------------------------------

Üzerinde **banka hesaplarını** sayfasında, oluşturulan her Havale dosyası için bir banka giderler havale ücretleri ayarlayabilirsiniz. Havale ücretleri havale onaylandığında ve gerçekleşen ücret tutarları bilindiğinde nakledilir. Havale ücretleri Müşterilerden toplanan ve günlük satırlarına iliştirilen ödeme masrafları farklıdır.
Kambiyo senetleri için belge düzenleri ayarlama
---------------------------------------------

Üzerinde **banka hesaplarını** sayfa, tıklatın **ayarlamak**ve yazdırılan kambiyo senedi oluşturacak olan her banka hesabı için belgeler için gerekli belge düzeni belirtin.
Kambiyo senetleri için müşteri ayarlama
--------------------------------------

Üzerinde **müşteriler** sayfasında, bir kambiyo senedi kullanarak ödeme kabul her müşteri için bir varsayılan ödeme yöntemi kambiyo senedi üzerinde ayarlayabilirsiniz **ödeme varsayılanları** sekme.




