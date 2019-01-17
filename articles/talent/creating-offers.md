---
title: "Teklifleri oluşturma, onaylama ve imzalama"
description: "Bu konu, Dynamics 365 for Talent kullanarak bir aday için teklif oluşturma, onaylama ve imzalama ayrıntılarını verir."
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-19
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: f189df052ef299a2cca1d92065a7a4d377d25399
ms.contentlocale: tr-tr
ms.lasthandoff: 12/07/2018

---

# <a name="creating-approving-and-signing-offers"></a>Teklifleri oluşturma, onaylama ve imzalama

[!include[banner](../includes/banner.md)]

Çoğu durumda, bir adaya teklif paketi hazırlama işlemi çok hızlı olması gerekir.
Attract yöneticisi tarafından ayarlanan şablonları kullanarak teklif oluşturanlar adaylara teklif hazırlama ve gönderme konusunda zamandan tasarruf eder ve daha az uğraşır.

## <a name="create-an-offer"></a>Teklif oluştur

Teklif yönetimi uygulaması açıldığında işe alım yöneticisi veya iş veren rolü olan herhangi bir kullanıcı, adaya bir teklif paketi hazırlayabilir. Teklifi hazırlamak için aşağıdakileri yapın.

1.  Teklifi için oluşturduğunuz aday başvurusuna ve işe gidin.

1.  **Teklif aşaması**'na gidin ve **Teklif hazırla**'ya tıklayın.

    Teklif uygulamasına yönlendirilecek ve burada adayı **Yeni** durumunda göreceksiniz. Oluşturan veya onaylayan olarak katkı sağladığınız diğer teklifleri de görebilirsiniz.

1.  **Teklif hazırla**'ya tıklayın. 
    
    Yönetici tarafından kullanılabilir olan farklı teklif paketleri görüntülenir.

1.  Bir paket seçin ve teklifi hazırlamaya başlamak için **Yapıldı** tıklayın.

    Teklif paketi şablonu, karşılık gelen işle ve teklifteki aday ayrıntılarıyla yüklenir.

1.  Teklif paketinin parçası olan tüm veri yer tutucuları giriş sayfasında görünür. Bu sayfada paketteki tüm değerleri doldurabilirsiniz.

    Giriş sayfasında, teklif paketinin parçası olan tüm teklif belge şablonlarını görebilirsiniz.

1.  Şimdi şablonun yönetici tarafından nasıl yapılandırıldığına bağlı olarak teklifin içeriğini düzenleyebilirsiniz.

1.  Gerekli olmayan olarak işaretlenmiş belgeleri kaldırmanız gerekirse, bunu yapabilirsiniz.

1. Doldurulan tüm teklif veri yer tutucuları oluşturulduğunda **Kaydet**'e tıklayın ve teklif taslağı kaydedin.

>[!NOTE]
> Taslak kaydedildikten sonra teklifin taslak sürümünü silebilir veya gerekirse yeni bir paket şablonu seçebilirsiniz.


## <a name="approve-an-offer"></a>Teklifi onayla

Çoğu teklif, teklifin gerekli standartları karşıladığından emin olmak için bir onay işlemi başlatmayı gerektirir. Bir teklif standartları karşılamazsa, örneğin teklif oluşturan teklif veri kurallarına uymazsa ve teklifkteki değerleri geçersiz kılarsa onay işlemi zorunludur. Bir teklifi onaya göndermek için aşağıdakileri yapın.

1.  Teklif taslak durumundayken onaylayanları **Onaylayan paneline** ekleyin. 
    >[!NOTE]
    > İşe alma müdürleri onaylayan olarak varsayılan olarak eklenir. Herhangi bir kullanıcıyı kuruluşunuzdan teklifi onaylayan olarak seçebilirsiniz.

1.  Gerekirse ardıl bir onaylama yöntemi veya paralel onay yöntemiyle onaylayanları atayın. Bu seçenek yalnızca yönetici tarafından bu şekilde yapılandırıldıysa kullanılabilirdir.
    >[!NOTE]
    > Onay işlemi sıralı ise, gerekirse, onaylayanların sırasını düzenleyebilirsiniz.

1.  Siz onay zincirini tanımlamayı bitirdiğinizde onay e-postası içeriğini düzenleyebilir ve sonra onaylayanlara bildirim gönderebilirsiniz. **Onaylayanlara gönder**' tıklayın.
    >[!NOTE]
    > Teklif standart dışıysa bir doğrulama sağlamanız gereklidir.

1.  Teklifi oluşturan onaylayanı atlamayı seçerse, bir not girebilir ve bir sonraki onaylayana atlayabilir.

Onaylayanlar, teklifi onaylamayı isteyen bir e-posta alır. Teklifi açmak, tüm teklif paketini gözden geçirmek, ya da teklif oluşturucusuna geri göndermek için e-postadaki bağlantıya tıklayabilirler. Teklif onaylayanların ise, teklif paketini daha fazla düzenleme için reddediyorsa başka bir not eklemesi gerekir. 

Teklifi onaylayanın eyleminden önce oluşturulan teklifin yeni bir sürümü olduğunda, onaylayanın teklifi onaylaması veya reddetmesi mümkün değildir.

## <a name="offer-versioning"></a>Teklif sürümü oluşturma 

Teklif onaylandığında veya sonraki düzenlemeler için geri gönderildiğinde **Düzenlemeyi etkinleştir**'i seçerek teklifin yeni bir sürümünü oluşturun. Teklifin yeni sürümü, tüm teklif veri değerlerine ve son sürümünden devreden onaylayanlar listesine sahiptir. 

Onaylayanlar, sürümler onay için kendileriyle paylaşılırsa farklı teklif sürümleri arasında geçiş yapabilir. Ayrıca, onaylayan veya teklif oluşturan bir önceki durumuna geri dönmek için bir özel taslak teklifi sürümü silmeyi tercih edebilir.


## <a name="send-an-offer-to-a-candidate"></a>Adaya teklif gönderin 

Teklif kaydedilmiş, onaylı ve adaya gönderilmesi için hazır olduğunda **Adaya gönder**'e tıklayın.

Teklifi adaya göndermeden önce yapmanız gereken birkaç eylem vardır.
-  Adaya gönderilecek teklif paketinin parçası olan belgelerin listesini görebilirsiniz.

-  Teklif bitiş tarihi belirtebilirsiniz. Adayların teklifi bitiş tarihinden önce kabul etmesi veya reddetmesi beklenir.  Adaya, teklif sona ermeden 48 saat önce bir anımsatıcı gönderilir.

-  Teklif onay işlemine dahil etmek istediğiniz ek belgeler olabilir. Gereken belge tipini listelemek için seçeneğiniz olacaktır.

- e-İmza seçeneği: Bir Adobe Sign, tercih edilen e-imza seçeneği olarak seçildiyse, oluşturuculara Adobe Sign lisanslarını bağlama seçeneği sunun. Bunu yapmak için iki yol vardır. **Teklif** içindeki Kullanıcı **Ayarları**'na gidin, **Bağlantılar** altında **Adobe Sign**'a bağlanın. Alternatif olarak, bağlantının kullanıcı ayarlarına göre zaten kurulu olmayan teklif Gönder aday ekrana bağlanmak istenir. 

> [!NOTE]
> Kullanıcılar yalnızca bir kez Adobe Sign hesaplarına bağlamanız gerekir. Aynı kullanıcı lisansı aynı kullanıcı tarafından gönderilir indirim gelecekteki tüm paketler için kullanılır. 

-  E-posta şablonu gerektiği gibi görüntüleyin ve düzenleyin.

Teklif hazır oldğunda ve **Adaya gönder**'e tıkladığınızda aday, teklifin gözden geçirilmeyi beklediğini belirten e-posta alır.


## <a name="candidates-actions-after-receiving-an-offer"></a>Teklif aldıktan sonra adayın eylemleri

Bir teklifin paylaşıldığı adaya bildirildikten sonra, başvuru panosuna gitmek ve teklifi görüntülemek için e-postalarındaki bağlantıyı tıklatabilir. Pano, adayın yine de tamamlaması gereken etkinlikleri gösterir.

1.  Teklif ve ilgili tüm belgeleri görüntülemek için aday **Teklifi görüntüle**'ye tıklatmalıdır.

    Adaylar, teklif paketini .zip biçiminde yükleyebilir.

1.  Teklifi kabul etmek için adayların teklif paketinin parçası olan her belge için **İmzaya geç**'e tıklaması gerekir.

1.  Tüm belgeler tek tek imzalanıp kabul edildiğinde adayın kabul işlemini bitirmek için sayfanın üstündeki **Teklifi kabul et**'e tıklaması gerekir.

1.  Teklifi reddetmek için adayın, sayfanın en üstündeki **Reddet**'e tıklaması, uygun nedeni seçmesi, gerekirse yorum eklemesi ve  **Reddet**'e tıklaması gerekir.

1.  Teklifi kabul veya reddettikten sonra aday, teklif görünümünde kalmayı veya başvuru panoya geri dönmeyi seçebilir.

1.  Teklif kabul işleminin bir parçası olarak istenen diğer belgeler varsa, aday gerektiği gibi belgeleri karşıya yüklemeyi ve istenen belge türü için etiketlemeyi seçmelidir.

1.  Teklifi oluşturan kişi tüm belgeler karşıya yüklendiğinde ve teklifi paketi imzalandığında bilgilendirilir.


## <a name="withdrawing-an-offer"></a>Teklifi geri çekme

Bir teklif, çeşitli nedenlerle herhangi bir aşamada adaydan geri çekilebilir. 
1.  Üç nokta düğmesine tıklatarak (**...**) ve ardından **Teklifi geri çek**'i tıklatarak teklifi geri çekin. 

2. Adayın durumundaki değişikliğiyle ilgili iletişime geçilip geçilmediğini soran bir ileti görüntülenir. Adayla daha önce bağlantı kurulmadıysa, aday için bunları daha ayrıntılı eylemleri bildiren bir e-posta gönder seçeneğini yüklemeniz gerekir. 

   Teklife artık aday tarafından erişilemez.


## <a name="closing-an-offer"></a>Teklifi kapatma 

Teklif kabul edildiğinde, reddedildiğinde veya geri alındığında ve başka eylemlere gerekli olmadığında, başka düzenlemeler yapılmaması için o teklif paketini kapatabilirsiniz.

