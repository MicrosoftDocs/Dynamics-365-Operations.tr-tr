---
title: Müşteri rehberliğine genel bakış
description: Bu konu, mağaza uygulamasında kullanılabilen yeni müşteri rehberliği yeteneklerine genel bir bakış sağlar.
author: bebeale
ms.date: 02/01/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom:
- "260624"
- intro-internal
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: b1e1b7a67141ffec01d926b7f917ebd4e1f24741
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984608"
---
# <a name="clienteling-overview"></a>Müşteri rehberliğine genel bakış

[!include [banner](includes/banner.md)]


Çoğu perakendeci, özellikle birinci sınıf uzman perakendeciler önemli müşterileriyle uzun vadeli ilişkiler kurabilecek satış yetkilileri ister. Yetkililerden, bu müşterilerin tercih ettiklerini ve etmediklerini, satın alma geçmişlerini, ürün tercihlerini ve yıldönümleriyle doğum günleri gibi önemli tarihlerini bilmeleri beklenir. Yetkililer bu bilgileri yakalayabilecekleri ve gerektiğinde kolayca bulabilecekleri bir yere ihtiyaç duyarlar. Bu bilgiler tek bir görünümde kullanılabilirse yetkililer, belirli ölçütleri karşılayan müşterileri kolayca hedefleyebilir. Örneğin, çanta alışverişi yapmayı tercih eden tüm müşterileri veya doğum günü ya da yıldönümü gibi yaklaşan önemli bir olayı olan müşterileri bulabilirler.

## <a name="client-book"></a>Müşteri defteri

Microsoft Dynamics 365 Commerce uygulamasında, perakendeciler mağaza yetkililerinin önemli müşterilerle uzun vadeli ilişkiler kurmasına yardımcı olmak için müşteri defteri işlevini kullanabilir.

Müşteri defteri, her müşterinin iletişim bilgilerini gösteren müşteri kartlarını ve perakendeci tarafından tanımlanan ve Headquarters'da yapılandırılan üç özelliği daha içerir. Perakendeciler, satış yetkililerinin müşteriler hakkında bilmesi gereken en önemli üç şeye karar verebilir. Örneğin, bir mücevher perakendecisi, insanların daha fazla mücevher satın alabileceği günler olan yıldönümleri veya doğum günleri gibi önemli tarihleri eklemek isteyebilir. Benzer şekilde, bir moda perakendecisi müşterinin tercih ettiği alışveriş ilgi alanlarını ve markalarını eklemek isteyebilir.

Müşteri defteri ayrıca satış yetkililerinin listeyi yalnızca belirli ölçütleri karşılayan müşterileri gösterecek şekilde filtrelemesine de olanak tanır. Örneğin, mağazaya yeni bir ayakkabı koleksiyonu geldi ve bir yetkili ayakkabı satın almayı tercih eden müşterileri bilgilendirmek istiyor. Bu durumda, yetkili ilgili müşterileri bulmak için müşteri defterini filtreleyebilir ve ardından başka eylemler gerçekleştirebilir.

Herhangi bir müşterinin bir nedenle artık önemli müşteri olarak kabul edilmemesi ve bu nedenle yakından yönetilmemesi gerekiyorsa satış yetkilileri, bunları müşteri defterlerinden kaldırabilir.

Bazı perakendeciler, müşterileri satış yetkilisi düzeyinde yönetmek istemez. Bunun yerine, önemli müşterilerin listesini mağaza düzeyinde yönetmek isterler. Bu perakendeciler müşterileri mağaza müşteri defterlerinden görüntüleyebilirler. Bu seçeneği kullanarak, perakendeciler adres defteri geçerli mağazanın adres defteriyle eşleşen tüm satış yetkililerinin müşteri defterlerindeki müşterileri görüntüleyebilir. Bu şekilde, bir yetkili tüzel kişiliğin sahip olduğu birden çok mağazada çalışıyorsa müşteri defteri tüm bu mağazalardaki müşterileri gösterir. Bu işlev ek yetenekleri destekler. Örneğin, müşteriler bir yetkiliden başka bir yetkiliye yeniden atanabilir. Bu yetenek, yetkililer transfer olduğunda veya şirketten ayrıldıklarında yararlıdır.

Her satış yetkilisi, her tüzel kişilik için bir müşteri defterine sahip olabilir ve yetkililer, müşteri defterlerine bir veya daha fazla müşteri ekleyebilir. Commerce'te, her müşteri şu anda yalnızca bir müşteri defterine eklenebilir. Ancak Microsoft, tek bir müşterinin birden çok müşteri defterine eklenmesine olanak tanıyan işlevler eklemeyi planlamaktadır.

> [!NOTE]
> Müşteri aramasından farklı olarak müşteri defteri, müşteri kayıtlarını mağazanın adres defterlerine göre filtrelemez.

## <a name="activities-and-notes"></a>Faaliyetler ve notlar

Çevrimiçi kanallar, perakendecilere müşterilerden açıkça bu bilgileri vermelerini istemeden müşteri tercihlerini öğrenme yolları sunar. Buna karşılık müşteriler mağazadaki satış yetkilileriyle etkileşime girdiğinde tercihleri hakkındaki bilgileri açıkça paylaşırlar. Ne yazık ki, bu bilgiler satıştan sonra kaybedilebilir. Ancak bu bilgiler kaydedilirse perakendecilerin müşterileri daha iyi anlamalarına ve bu şekilde daha iyi öneriler ve daha iyi bir genel alışveriş deneyimi sunmalarına yardımcı olabilir.

Satış yetkilileri müşterilerin paylaştığı önemli bilgileri yakalamak için yalnızca müşteri defteri özniteliklerini değil aynı zamanda faaliyetler ve notlar işlevini de kullanabilir. Perakendeciler, mağaza ziyareti hakkında bilgiler, e-posta adresi, telefon numarası ve randevular gibi faaliyet türlerini yapılandırabilir. Yetkililerin oluşturduğu faaliyetler, satış noktasında (POS) bir zaman çizelgesi biçiminde görüntülenebilir. Ayrıca Headquarters'ta **Tüm müşteriler \> Genel** sayfasındaki **Faaliyetler** sekmesinde de görüntülenebilirler.

Satış yetkilileri, her etkileşimden önce başvurulabilecek genel müşteri bilgilerini yakalamak için notları da kullanabilir. Bu notlar Headquarters'ta kaydedilir ve müşteri profilinde veya çağrı merkezindeki müşteri ayrıntıları sayfasında görüntülenebilir.

> [!NOTE]
> Şu anda, tüm notlar ve faaliyetler tüzel kişilik için çalışan ve müşteri ayrıntıları sayfalarını görüntüleyebilen satış yetkilileri tarafından görüntülenebilir. Notlar ve faaliyetler, müşteri defterine müşteri ekleyen yetkiliyle sınırlı değildir.

## <a name="integration-with-dynamics-365-customer-insights"></a>Dynamics 365 Customer Insights'le Tümleştirme

Perakendeciler Dynamics 365 Customer Insights uygulamasını kullanarak müşterilerin perakendecinin markasıyla etkileşim kurmak için kullandıkları çeşitli sistemlerden veri toplayabilir. Ardından bu verileri müşterinin tek bir görünümünü oluşturmak ve öngörüler türetmek için kullanabilirler. Customer Insights'ın Commerce ile tümleştirilmesi, perakendecilerin müşteri defterindeki müşteri kartında gösterilmesi gereken bir veya daha fazla ölçümü seçmelerine olanak tanır. Örneğin, perakendeciler bir müşteri için "kayıp olasılığını" hesaplamak ve "sonraki en iyi eylemi" tanımlamak için Customer Insights'taki verileri kullanabilir. Bu değerler ölçüm olarak tanımlanırsa müşteri kartında gösterilebilir ve satış yetkililerine önemli bilgiler sağlayabilir. Customer Insights hakkında daha fazla bilgi için [Dynamics 365 Customer Insights](/dynamics365/ai/customer-insights/overview) belgelerine bakın. Ölçümler hakkında daha fazla bilgi için bkz. [Ölçümler](/dynamics365/ai/customer-insights/pm-measures).

## <a name="set-up-clienteling"></a>Müşteri rehberliğini ayarlama

Ortamınızda müşteri rehberliği işlevini açmak için aşağıdaki adımları izleyin.

1. **Özellik yönetimi** çalışma alanında, özellikleri **Perakende ve ticaret** modülüne göre filtreleyin.

    ![Commerce modülü için özellikler listesinde müşteri rehberliği.](./media/Enable_clienteling.png "Perakende ve ticaret modülü için özellikler listesinde müşteri rehberliği")

2. **Şimdi etkinleştir** öğesini seçerek **Müşteri rehberliği** özelliğini açın.
3. **Commerce Parametreleri** sayfasında, **Numara serisi** sekmesinde, **Müşteri defteri tanımlayıcısı** satırını seçin. Ardından **Numara serisi kodu** alanından bir numara serisi seçin. Sistem, bu numara serisini müşteri defterlerine bir kod atamak için kullanır.
4. **Kaydet**'i seçin.
5. Müşteri defterlerinde yönetilen müşteriler için yakalamak istediğiniz öznitelikleri içeren yeni bir öznitelik grubu oluşturun. Yönergeler için bkz. [Öznitelikler ve öznitelik grupları](./attribute-attributegroups-lifecycle.md).

    - Gerekli öznitelikleri **İyileştirilebilir** olarak tanımlayın. Satış yetkilileri daha sonra bu öznitelikleri müşteri defterlerini filtrelemek için kullanabilir.
    - Bu öznitelikler için görüntüleme sırası ayarlayın. Bu görüntüleme sırası, müşteri defterindeki müşteri kartında hangi özniteliklerin gösterilmesi gerektiğini belirler. Görüntüleme sırası 1'in görüntüleme sırası 2'den yüksek olduğu kabul edilir. Bu nedenle, görüntüleme sırası 1 olan öznitelik, görüntüleme sırası 2 olan öznitelikten önce görüntülenir.

    > [!NOTE]
    > Customer Insights'ı aynı sayfadan kullanılabilir hale getirebilirsiniz. Ancak kimlik doğrulama amacıyla bir Azure uygulama kodu ve parola oluşturulmalıdır. (Gereksinimler hakkında bilgi için bu konunun ilerleyen bölümlerindeki [Customer Insights'ın Commerce ile tümleştirilmesini açma](#turn-on-the-integration-of-customer-insights-with-commerce) bölümüne bakın.) Customer Insights açıksa ve müşteri kartında gösterilmesi gereken bir veya daha fazla ölçümü seçtiyseniz bu ölçümler önce gösterilir. Ardından görüntüleme sırasına göre müşteri defteri öznitelik grupları gösterilir. Örneğin, Customer Insights'tan iki ölçüm seçerseniz müşteri kartında bu iki ölçüm ve bir müşteri defteri özniteliği gösterilir. (Gösterilen müşteri defteri özniteliği, en yüksek görüntüleme sırasına sahip özniteliktir.)

6. **Commerce parametreleri** sayfasında, **Müşteri rehberliği** sekmesinde, **Müşteri defteri öznitelik grubu** alanında, oluşturduğunuz öznitelik grubunu seçin.

    ![Seçilen müşteri defteri öznitelik grubu.](./media/Client%20book%20attributes.png "Seçilen müşteri defteri öznitelik grubu")

7. POS'ta gerçekleşen faaliyetleri yakalamak için **Faaliyet türleri** sayfasında (**Retail and Commerce \> Müşteriler \> Faaliyet türleri**) faaliyet türlerini tanımlayın.

    > [!NOTE]
    > Faaliyet türleri, gerçek zamanlı arama ilk yapıldığında Commerce Scale Unit tarafından çekilir. Faaliyetler çekildikten sonra birkaç saatliğine önbelleğe alınır. Faaliyet türlerini değiştirirseniz önbellek artık geçerli olmayana kadar bekleyin. Alternatif olarak, üretim dışı ortamlarda Commerce Scale Unit hizmetini yeniden başlatın.

8. Satış yetkililerinin kendi müşteri defterlerini ve mağaza müşteri defterlerini görüntüleyebilmeleri için uygun POS ekranı düzenine iki düğme ekleyin. (Mağaza müşteri defterleri, bir adres defterini mağaza ile paylaşan tüm yetkililerin tüm müşteri defterlerindeki müşterileri içerir.) Karşılık gelen işlemler sırasıyla **Müşteri defterinde müşterileri görüntüle** ve **Mağaza müşteri defterlerinde müşterileri görüntüle** olarak adlandırılır. Müşteri defterleriyle ilgili üç ek işlem kullanılabilir. Bu işlemler, hangi yetkililerin müşteri defterinden müşteri ekleyebileceğini, kaldırabileceğini ve yeniden atayabileceğini belirler. Bunlar sırasıyla **Müşteriyi müşteri defterine ekle**, **Müşterileri müşteri defterinden kaldır** ve **Müşterileri müşteri defterine yeniden ata** olarak adlandırılır.
9. Aşağıdaki dağıtım planı işlerini çalıştırın: 1040, 1150, 1110 ve 1090.

Bu yordamı tamamladıktan sonra, satış yetkilileri POS'ta müşteri ayrıntıları sayfasını açabilir ve müşteri defterlerine müşteriler ekleyebilir, müşteriler için faaliyetleri ve notları görüntüleyip yakalayabilir ve müşteri defterini filtrelemek için müşteri ve müşteri defteri özniteliklerini kullanarak müşterileri hedefleyebilir. Aşağıdaki şekilde bir müşteri defteri örneği gösterilmiştir.

![Müşteri defteri örneği.](./media/client_book.png "Müşteri defteri örneği")

## <a name="turn-on-the-integration-of-customer-insights-with-commerce"></a>Customer Insights'ın Commerce ile tümleştirilmesini açma

Customer Insights'ın Commerce ile tümleştirilmesini açmak için Commerce'in kullanıldığı kiracıda etkin bir Customer Insights kurulumunuzun olduğundan emin olmanız gerekir. Ayrıca Azure aboneliğinin bulunduğu bir Azure Active Directory (Azure AD) kullanıcı hesabınızın olması gerekir.

Tümleştirmeyi ayarlamak için aşağıdaki adımları izleyin.

1. Azure portalda, yeni bir uygulama kaydedin ve uygulama adını, uygulama kimliğini ve gizli diziyi not edin. Bu bilgiler, Commerce ve Customer Insights arasında hizmetten hizmete kimlik doğrulaması için kullanılacaktır. Anahtar kasasına kaydetmek için gerekli olacağından gizli diziyi güvenli bir şekilde not edin. Aşağıdaki örnekte, sırasıyla uygulama adı, uygulama kimliği ve gizli dizi için CI_Access_name, CI_Access_AppID, CI_Access_Secret kullanın. Daha fazla bilgi için bkz. [Hızlı başlangıç: Microsoft kimlik platformu ile bir uygulamayı kaydetme](/azure/active-directory/develop/quickstart-register-app).

    > [!IMPORTANT]
    > Süresi dolmadan parolayı değiştirdiğinizde anımsayabilmenizi sağlayacak adımları atın. Aksi takdirde, tümleştirme beklenmedik şekilde durdurulur.

2. Customer Insights bulut sunucunuza gidin ve yukarıda oluşturulan uygulamanın adını arayın (bu örnekte "CI_Access_name").
3. Bir Azure Key Vault oluşturup adı ve URL'yi not edin (bu örnekte, "KeyVaultName", "KeyVaultURL"). Yönergeler için bkz. [Hızlı Başlangıç: Azure portalını kullanarak Azure Anahtar Kasasında bir parola ayarlama ve alma](/azure/key-vault/quick-create-portal).
4. Kasaya gizli diziyi (bu örnekte "CI_Access_Secret") kaydedin. Bu gizli dizi kasada saklandığında, gizli dizi bir isim alır. Gizli dizi adını not edin (bu örnekte, "SecretName").
5. Azure Key Vault'tan gizli diziye erişmek için, uygulama kimliği ve gizli dizi (bu örnekte "KeyVault_Access_AppID" ve "KeyVault_Access_Secret") ile başka bir uygulama oluşturmanız gerekir. Bir daha görüntülenmeyeceği için gizli diziyi güvenli bir şekilde not edin.
6. Ardından, API'leri kullanarak Key Vault'a Commerce'den erişmek için uygulamaya izin vermeniz gerekir. Azure portalda uygulama sayfasına gidin. **Yönet** bölümünün altında **API izinleri**'ni seçin. **Azure Key Vault**'a erişim için izin ekleyin. Bu izin için **Erişim ilkesi** seçin. Şablonu **Gizli dizi yönetimi** olarak seçin ve **Al**, **Listele**, **Şifresini Çöz** ve **Şifrele** seçeneklerini belirleyin. 
5. Commerce Headquarters'da, **Sistem yönetimi \> Kurulum \> Key Vault parametreleri**'ne gidin ve anahtar kasası için gerekli bilgileri girin. Ardından Commerce'in anahtar kasasındaki parolalara erişebilmesi için **Anahtar Kasası istemcisi** alanına, 4. adımda kullandığınız uygulama kodunu girin.
6. 1. adımda oluşturduğunuz uygulamayı güvenli uygulamalar listesine (bazen güvenli liste olarak da adlandırılır) eklemek için Customer Insights'a gidin ve uygulamaya **Görüntüleme** erişimini seçin. Yönergeler için bkz. [İzinler](/dynamics365/ai/customer-insights/pm-permissions).
7. Commerce HQ'daki **Sistem yönetimi > Kurulum > Key Vault parametreleri** sayfasında, alanları aşağıda açıklandığı gibi güncelleştirin: 

- **Key Vault URL'si**: "KeyVaultURL" (yukarıdaki 3. adımda).
- **Key Vault istemcisi**: "KeyVault_Access_AppID" (yukarıdaki 5. adımda).
- **Key Vault gizli anahtarı**: "KeyVault_Access_Secret" (yukarıdaki 5. adımda).
- **Gizli Diziler** bölümünün altında:
    - **Ad**: Herhangi bir ad, örneğin "CISecret".
    - **Açıklama**: Herhangi bir değer.
    - **Gizli dizi**: **kasa**:`//<Name of key vault>/<name of secret>>` Bu örnekte `vault://KeyVaultName/SecretName` olacaktır.

Alanları güncelleştirdikten sonra, gizli diziye Commerce uygulaması tarafından erişilebildiğinden emin olmak için **Doğrula**'yı seçin.

8. Commerce'de, **Commerce parametreleri** sayfasında, **Müşteri Tabanı** sekmesinde, **Dynamics 365 Customer Insights** hızlı sekmesinde, **Uygulama Kimliği**'ni "CI_Access_AppID" olarak ayarlayın (yukarıdaki adım 1'de). **Gizli dizi adı** için yukarıdaki 7. adımda girilen gizli dizi adını ("CISecret") seçin. **Customer Insights'ı etkinleştir** seçeneğini **Evet** olarak ayarlayın. Kurulum herhangi bir nedenle başarısız olursa bir hata iletisi görüntülenir ve bu seçenek **Hayır** olarak ayarlanır. 

Customer Insights'ta test ve üretim ortamları gibi birden çok ortama sahip olabilirsiniz. **Ortam kurulumu kodu** alanına, uygun ortamı girin. **Alternatif müşteri kodu** alanına, Customer Insights'ta müşteri hesap numarasıyla eşleşen özelliği girin. (Commerce'de, müşteri hesap numarası müşteri kimliğidir.) Kalan üç özellik, müşteri defterindeki müşteri kartında gösterilecek ölçülerdir. Müşteri kartında gösterilmek üzere en fazla üç ölçüm seçebilirsiniz. Ancak, herhangi bir ölçü seçmeniz gerekmez. Daha önce de belirtildiği gibi, sistem önce bu değerleri gösterir ve sonra müşteri defteri öznitelik grubunun değerlerini gösterir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]