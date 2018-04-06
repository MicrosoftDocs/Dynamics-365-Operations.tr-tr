---
title: "Gelişmiş banka mutabakatı kullanarak banka ekstreleri arasında mutabakat sağlayın"
description: "Gelişmiş banka mutabakatı özelliği, elektronik banka ekstrelerini içe aktarmanıza ve bunların Microsoft Dynamics 365 for Finance and Operations uygulamasındaki banka hareketleriyle otomatik olarak mutabakat sağlamasına izin verir. Bu konuda mutabakat işlemi açıklanmaktadır."
author: saraschi2
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationWorksheet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ed3a1fae6ca30b9411fde47e7ef8a08150d7d748
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Gelişmiş banka mutabakatı kullanarak banka ekstreleri arasında mutabakat sağlayın

[!include[banner](../includes/banner.md)]


Gelişmiş banka mutabakatı özelliği, elektronik banka ekstrelerini içe aktarmanıza ve bunların Microsoft Dynamics 365 for Finance and Operations uygulamasındaki banka hareketleriyle otomatik olarak mutabakat sağlamasına izin verir. Bu konuda mutabakat işlemi açıklanmaktadır.  

<a name="import-an-electronic-bank-statement"></a>Elektronik banka ekstresini içe aktarma
-----------------------------------

**Banka ekstreleri** sayfasındaki **Ekstreyi içe aktar** eylemini kullanarak banka ekstrelerini içe aktarın. Banka ekstresinde, banka hesabı, banka hesap ayrıntılarına ayarlanan değer birleşimleri aracılığıyla tanımlanır. Bu değerler banka adı, banka hesap numarası, rota numarası, Dünya Interbank Mali Telekomünikasyon Derneği (SWIFT) kodu ve Uluslararası Banka Hesap Numarasını (IBAN) içerir. 

Tek bir hesap veya birden fazla hesapla ilgili bilgileri içeren bir banka ekstresini karşıdan yükleyebilirsiniz. Birden fazla hesap varsa hesaplar farklı tüzel kişiliklerde olabilir.

-   Tek bir banka hesabına ait tek bir banka ekstresi dosyasını içe aktarmak için **Tüm tüzel kişiliklerde birden fazla banka hesabına ait ekstreyi içe aktar** seçeneğini **Hayır** olarak ayarlayın ve ekstreyle ilişkili banka hesabını seçin. İlişkili banka ekstresi dosyasını seçmek için **Gözat**'a tıklayın ve sonra **Yükle**'ye tıklayın.
-   Birden fazla hesaba ait tek bir banka ekstresi dosyasını içe aktarmak için **Tüm tüzel kişiliklerde birden fazla banka hesabına ait ekstreyi içe aktar** seçeneğini **Evet** olarak ayarlayın. İlişkili banka ekstresi dosyasını seçmek için **Gözat**'a tıklayın ve sonra **Yükle**'ye tıklayın.

Elektronik dosyadaki ekstreler tanımlayıcı alanlar kullanılarak bir banka hesabı ile ilişkilendirilemiyorsa bunlar içe aktarılmaz. Ancak dosyadaki diğer ekstreler içe aktarılabilir. Daha sonra kullanıcı banka ekstrelerini içe aktarma işleminin belirli banka hesapları için başarısız olduğunu bildiren bir ileti alır. Banka ekstresi dosyasını içe aktaran kullanıcının tüzel kişiliğin banka hesaplarına ait ekstreleri içe aktarma erişiminin olması gerektiğini unutmayın. 

Birden fazla ekstre dosyasını Finance and Operations uygulamasına tek bir işlemde yüklemek için bir zip dosyası kullanabilirsiniz. Birden fazla hesaba ait birden fazla banka ekstresi dosyasını içe aktarmak için tüm banka ekstresi dosyalarını bir zip dosyasında birleştirin. **Banka ekstrelerini içeri aktar** iletişim kutusundaki **Tüm tüzel kişiliklerde birden fazla banka hesabına ait ekstreyi içe aktar** seçeneğini **Evet** olarak ayarlayın. Banka ekstresi dosyalarını içeren zip dosyasını seçmek için **Gözat**'a tıklayın ve sonra **Yükle**'ye tıklayın. İçe aktarma işlemi zip dosyasını tanır ve banka hesabının tüzel kişiliğinden bağımsız olarak, içindeki her ekstreyi karşıya yükler. 

**İçe aktarmadan sonra mutabakat sağla** seçeneği kullanılabilir. Bu seçeneği **Evet** olarak ayarladığınızda, sistem banka ekstresini otomatik olarak doğrular, yeni banka mutabakatını ve çalışma sayfasını oluşturur ve banka ekstresi karşıya yüklendiğinde Varsayılan eşleştirme kural kümesini çalıştırır. Bu işlevler işlemi hareketlerin el ile eşleştirilmesi gereken noktaya kadar otomatik hale getirir.

## <a name="validate-the-bank-statement"></a>Banka ekstresini doğrulama
Bir ekstreyi doğrulamak için **Banka ekstreleri** sayfasında, **Doğrula**'ya tıklayın. Mutabakatları sağlanmadan önce banka ekstreleri doğrulanmalıdır. İçe aktarma zamanında **İçe aktarmadan sonra mutabakat sağla** seçeneğini **Evet** olarak ayarladıysanız bu adım otomatik olarak tamamlanır. 

Banka ekstresi doğrulama aşağıdaki ayrıntıları doğrular:

-   Banka ekstresi seçili banka hesabıyla eşleşir.
-   Banka ekstresi para birimi banka hesabı para birimiyle eşleşir.
-   Ekstrenin açılış bakiyesi banka hesabına ait önceki ekstrenin kapanış bakiyesine eşittir.
-   Tarih, aynı banka hesabına ait farklı bir banka ekstresi tarihiyle çakışmaz.
-   Banka hesabına ait ekstrelerin tarihlerinde boşluklar yoktur.
-   Ekstre satırlarındaki tarihler banka ekstresinin başlangıç tarihi ile bitiş tarihi arasındadır.
-   Açılış bakiyesi ve özetlenmiş satır tutarları kapanış bakiyesine eşittir.

Doğrulama tamamlandığında banka ekstresinin durumu **Doğrulandı** olarak güncelleştirilir. Banka ekstresi, mutabakatı sağlanmadan önce doğrulanmalıdır.

## <a name="reconcile-the-bank-statement"></a>Banka ekstresi mutabakatı sağlayın
Elektronik banka ekstresini içe aktardıktan ve **Banka ekstreleri** sayfasında doğruladıktan sonra **Banka mutabakatı** ve **Banka mutabakatı çalışma sayfası** sayfalarını kullanarak banka ekstresi mutabakatı sağlayabilirsiniz. 

Yeni bir mutabakat oluşturmak için **Banka mutabakatı** sayfasında **Yeni**'ye tıklayın ve sonra içe aktarılan ekstrenin banka hesabını seçin. Bir banka hesabı yalnızca bir açık banka mutabakatına sahip olabilir. Sonlanma tarihi, mutabakat çalışma sayfasına dahil edilen banka ekstresi hareketlerini ve Operations banka hareketlerini belirler. Varsayılan olarak, geçerli sistem tarihi sonlanma tarihi olarak kullanılır ancak mutabakat için tarihi değiştirebilirsiniz. Kalan başlık bilgileri ekstreden otomatik olarak alınır. İçe aktarma zamanında **İçe aktarmadan sonra mutabakat sağla** seçeneğini **Evet** olarak ayarladıysanız bu adım otomatik olarak tamamlanır. 

**Banka mutabakatı çalışma sayfasını** açmak için **Banka mutabakatı** sayfasında **Çalışma sayfası**'na tıklayın. **İçe aktarmadan sonra mutabakat sağla** seçeneğini **Evet** olarak ayarladıysanız Varsayılan eşleştirme kural kümesi mutabakat için otomatik olarak çalıştırılır. Eşleştirme kurallarını el ile çalıştırmak için banka hareketlerine göre eşleştirme kural kümeleri veya eşleştirme kurallarını seçerek **Eşleştirme kurallarını çalıştır**'a tıklayın. İşleme ait çok fazla hareketiniz varsa bu adımı toplu iş işlemi olarak tamamlayabilirsiniz. 

**Banka mutabakatı çalışma sayfası** hareketleri içeren dört kılavuza sahiptir. İki üst kılavuz banka ekstresinden ve Operations'dan gelen henüz eşleştirilmemiş hareketleri gösterir. İki alt kılavuz eşleştirilmiş hareketleri gösterir. **Banka ekstresi hareket ayrıntıları** sekmesi üst kılavuzda seçilen eşleştirilmemiş banka ekstresi hareketi için ayrıntıları gösterir. 

Banka ekstresi hareketlerini eşleştirmek veya mutabakatlarını sağlamak için üç yol vardır:

-   Hareketleri Operations banka hareketleriyle eşleştirin.
-   Hareketleri ters banka ekstresi hareketiyle eşleştirin.
-   Hareketleri, daha sonra Finance and Operations uygulamasında bir banka hareketi olarak nakledilebilmeleri için **Yeni** olarak işaretleyin.

Hareketleri el ile eşleştirmek için **Banka ekstresi hareketleri** kılavuzundaki hareketleri seçin, **Operations banka hareketleri** kılavuzundaki ilgili hareketleri seçin ve sonra **Eşleştir**'e tıklayın. Seçili hareketler eşleşmemiş hareketler için olan üst kılavuzlardan eşleşmiş hareketler için olan alt kılavuzlara taşınır. Buna ek olarak, eşleşen ve eşleşmeyen toplam tutarlar güncelleştirilir. Bire bir, çoğa bir ve çoğa çok hareket eşleştirmelerine sahip olabilirsiniz. Eşleştirmeler izin verilen tarih farkı ve hareket türü eşleşmesine dair kurallara uymalıdır. Bu kurallar **Nakit ve banka yönetimi parametreleri** sayfasından ayarlanır.

Mutabakatınızda kuruş farkları oluşabilir. Kuruş farkları, banka hesabındaki **İzin verilen kuruş farkı** alanı tarafından tanımlanan tolerans tutarı dahilinde ise kuruş farkına sahip tek bir banka ekstresini ve tek bir Operations banka hareketini eşleştirebilirsiniz. Tutar, eşleşen Operations banka hareketlerinde **Düzeltme tutarı** alanında gösterilir. Banka mutabakatı mutabakat sağlandı olarak işaretlendiğinde, düzeltmeler ilişkili banka hareketi türü ile tanımlanan ana hesap kullanılarak otomatik olarak deftere nakledilir. **Çek** ve **Havale** belge türleri için düzeltmeler desteklenmez. 

Banka ekstresi hareket ters işlemleri mutabakat çalışma sayfasını kullanarak eşleştirilir. Tutarlar ters ise ve hareketlerden biri ters işlem olarak işaretlenmişse iki ekstre satırı eşleştirilebilir. Ayrıca **Ters işlem ekstresi satırlarını temizle** eylemi için bir eşleştirme kuralı ayarlayabilirsiniz.

Tersine çevrilmiş Operations banka hareketleri için **Operations banka hareketleri** sayfası kullanılarak mutabakat sağlanmalıdır. Belgeler aynı banka hesabı, belge türü ve ödeme referansına sahipse ve bunlar ters tutarlara sahipse iki Operations banka hareketini birlikte mutabık kılabilirsiniz. Ayrıca bu hareketlerin mutabakat çalışma sayfasında görünmesini önlemek için tek bir iptal edilmiş çeki mutabık kılabilirsiniz. 

Finance and Operations uygulamasında henüz bulunmayan faiz, ücretler ve masraflar gibi yeni başlatılan bir banka hareketi varsa seçili banka ekstresi mutabakatıyla ilişkili bir günlüğe bunları ekleyebilirsiniz. Eşleşmemiş işlemler için **Banka ekstresi hareketleri** kılavuzunu seçin ve sonra **Yeni olarak işaretle**'ye tıklayın. Hareket durumu **Yeni** olarak ayarlanır ve hareket eşleşmiş hareketler için **Banka ekstresi hareketleri** kılavuzuna taşınır. Sonra **Yeni** olarak işaretlenmiş hareketleri **Banka ekstresi** sayfasından nakledin. 

Hatalı eşleşmiş hareketlerin eşleşmesini kaldırabilirsiniz. Eşleşen banka ekstresi hareketini seçin ve sonra **Eşleşmeyi kaldır**'a tıklayın. Tüm ilişkili hareketler eşleşmemiş hareketler için üst kılavuzlara geri taşınır ve eşleşmiş ve eşleşmemiş toplam tutarlar güncelleştirilir. 

Mutabakat işleminiz tamamlandıktan sonra Banka mutabakat çalışma sayfasını mutabakat sağlandı olarak işaretlemeniz gerekir.  Bu işlem otomatik olarak düzeltme tutarlarını, **Banka hareket türü** sayfasında ayarlanan hesapları kullanarak işleyecektir.  Bir ekstre için banka mutabakatı, herhangi bir zamanda mutabakat edilmiş olarak işaretlenebilir, henüz eşlenmemiş banka ekstresi satırları olsa bile.  Eşleşmemiş hareketler otomatik olarak bir sonraki mutabakat çalışma sayfasına, eşlenmemiş banka ekstresi hareketleri olarak taşınır.  Banka ekstresi mutabakatının, mutabakat edilmiş olarak işaretlendiğinde geri alınamayacağını unutmayın.  Mutabakat, artık düzenlenebilir olmayacaktır ve bu mutabakata güncelleştirmeler yapma olanağınız olmayacaktır.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Mutabakatla ilişkili yeni hareketleri nakletme
Mutabakat çalışma sayfasında **Yeni** olarak işaretlediğiniz banka ekstresi hareketleri **Banka ekstresi** sayfasında nakledilir. **Banka ekstresi** sayfasında ekstre ayrıntılarını görüntülemek için ekstre kimliğini seçin. Yeni hareketler ve ilişkili muhasebe girişleri haricindeki ayrıntıları görüntülemek için **Muhasebe** menüsündeki **Dağıtımları görüntüle** ve **Muhasebeyi görüntüle** seçeneklerini kullanabilirsiniz. **Yeni** olarak işaretlenmiş banka ekstresi satırlarını genel muhasebeye nakletmek için **Naklet** seçeneğini seçin. Deftere naklin banka ekstresi başına yalnızca tek seferde tamamlanabildiğini unutmayın.




