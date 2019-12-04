---
title: Müşteri rehberliğine genel bakış
description: Bu konu, perakende mağaza uygulamasında kullanılabilen yeni müşteri rehberliği yeteneklerine genel bir bakış sağlar.
author: bebeale
manager: AnnBe
ms.date: 11/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: fb58022f61f9944d6e385874db1f2342bc111866
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774073"
---
# <a name="clienteling-overview"></a>Müşteri rehberliğine genel bakış

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Çoğu perakendeci, özellikle birinci sınıf uzman perakendeciler önemli müşterileriyle uzun vadeli ilişkiler kurabilecek satış yetkilileri ister. Yetkililerden, bu müşterilerin tercih ettiklerini ve etmediklerini, satın alma geçmişlerini, ürün tercihlerini ve yıldönümleriyle doğum günleri gibi önemli tarihlerini bilmeleri beklenir. Yetkililer bu bilgileri yakalayabilecekleri ve gerektiğinde kolayca bulabilecekleri bir yere ihtiyaç duyarlar. Bu bilgiler tek bir görünümde kullanılabilirse yetkililer, belirli ölçütleri karşılayan müşterileri kolayca hedefleyebilir. Örneğin, çanta alışverişi yapmayı tercih eden tüm müşterileri veya doğum günü ya da yıldönümü gibi yaklaşan önemli bir olayı olan müşterileri bulabilirler.

## <a name="client-book"></a>Müşteri defteri

Microsoft Dynamics 365 Retail uygulamasında, perakendeciler mağaza yetkililerinin önemli müşterilerle uzun vadeli ilişkiler kurmasına yardımcı olmak için müşteri defteri işlevini kullanabilir.

Müşteri defteri, her müşterinin iletişim bilgilerini gösteren müşteri kartlarıyla birlikte perakendeci tarafından tanımlanan ve Retail Headquarters'ta yapılandırılmış üç ek özellik içerir. Perakendeciler, satış yetkililerinin müşteriler hakkında bilmesi gereken en önemli üç şeye karar verebilir. Örneğin, bir mücevher perakendecisi, insanların daha fazla mücevher satın alabileceği günler olan yıldönümleri veya doğum günleri gibi önemli tarihleri eklemek isteyebilir. Benzer şekilde, bir moda perakendecisi müşterinin tercih ettiği alışveriş ilgi alanlarını ve markalarını eklemek isteyebilir.

Müşteri defteri ayrıca satış yetkililerinin listeyi yalnızca belirli ölçütleri karşılayan müşterileri gösterecek şekilde filtrelemesine de olanak tanır. Örneğin, mağazaya yeni bir ayakkabı koleksiyonu geldi ve bir yetkili ayakkabı satın almayı tercih eden müşterileri bilgilendirmek istiyor. Bu durumda, yetkili ilgili müşterileri bulmak için müşteri defterini filtreleyebilir ve ardından başka eylemler gerçekleştirebilir.

Herhangi bir müşterinin bir nedenle artık önemli müşteri olarak kabul edilmemesi ve bu nedenle yakından yönetilmemesi gerekiyorsa satış yetkilileri, bunları müşteri defterlerinden kaldırabilir.

Bazı perakendeciler, müşterileri satış yetkilisi düzeyinde yönetmek istemez. Bunun yerine, önemli müşterilerin listesini mağaza düzeyinde yönetmek isterler. Bu perakendeciler müşterileri mağaza müşteri defterlerinden görüntüleyebilirler. Bu seçeneği kullanarak, perakendeciler adres defteri geçerli mağazanın adres defteriyle eşleşen tüm satış yetkililerinin müşteri defterlerindeki müşterileri görüntüleyebilir. Bu şekilde, bir yetkili tüzel kişiliğin sahip olduğu birden çok mağazada çalışıyorsa müşteri defteri tüm bu mağazalardaki müşterileri gösterir. Bu işlev ek yetenekleri destekler. Örneğin, müşteriler bir yetkiliden başka bir yetkiliye yeniden atanabilir. Bu yetenek, yetkililer transfer olduğunda veya şirketten ayrıldıklarında yararlıdır.

Her satış yetkilisi, her tüzel kişilik için bir müşteri defterine sahip olabilir ve yetkililer, müşteri defterlerine bir veya daha fazla müşteri ekleyebilir. Retail'de, her müşteri şu anda yalnızca bir müşteri defterine eklenebilir. Ancak Microsoft, tek bir müşterinin birden çok müşteri defterine eklenmesine olanak tanıyan işlevler eklemeyi planlamaktadır.

> [!NOTE]
> Müşteri aramasından farklı olarak müşteri defteri, müşteri kayıtlarını mağazanın adres defterlerine göre filtrelemez.

## <a name="activities-and-notes"></a>Faaliyetler ve notlar

Çevrimiçi kanallar, perakendecilere müşterilerden açıkça bu bilgileri vermelerini istemeden müşteri tercihlerini öğrenme yolları sunar. Buna karşılık müşteriler mağazadaki satış yetkilileriyle etkileşime girdiğinde tercihleri hakkındaki bilgileri açıkça paylaşırlar. Ne yazık ki, bu bilgiler satıştan sonra kaybedilebilir. Ancak bu bilgiler kaydedilirse perakendecilerin müşterileri daha iyi anlamalarına ve bu şekilde daha iyi öneriler ve daha iyi bir genel alışveriş deneyimi sunmalarına yardımcı olabilir.

Satış yetkilileri müşterilerin paylaştığı önemli bilgileri yakalamak için yalnızca müşteri defteri özniteliklerini değil aynı zamanda faaliyetler ve notlar işlevini de kullanabilir. Perakendeciler, mağaza ziyareti hakkında bilgiler, e-posta adresi, telefon numarası ve randevular gibi faaliyet türlerini yapılandırabilir. Yetkililerin oluşturduğu faaliyetler, satış noktasında (POS) bir zaman çizelgesi biçiminde görüntülenebilir. Ayrıca Retail Headquarters'ta **Tüm müşteriler \> Genel** sayfasındaki **Faaliyetler** sekmesinde de görüntülenebilirler.

Satış yetkilileri, her etkileşimden önce başvurulabilecek genel müşteri bilgilerini yakalamak için notları da kullanabilir. Bu notlar Retail Headquarters'ta kaydedilir ve müşteri profilinde veya çağrı merkezindeki müşteri ayrıntıları sayfasında görüntülenebilir.

> [!NOTE]
> Şu anda, tüm notlar ve faaliyetler tüzel kişilik için çalışan ve müşteri ayrıntıları sayfalarını görüntüleyebilen satış yetkilileri tarafından görüntülenebilir. Notlar ve faaliyetler, müşteri defterine müşteri ekleyen yetkiliyle sınırlı değildir.

## <a name="integration-with-dynamics-365-customer-insights"></a>Dynamics 365 Customer Insights'le Tümleştirme

Perakendeciler Dynamics 365 Customer Insights uygulamasını kullanarak müşterilerin perakendecinin markasıyla etkileşim kurmak için kullandıkları çeşitli sistemlerden veri toplayabilir. Ardından bu verileri müşterinin tek bir görünümünü oluşturmak ve öngörüler türetmek için kullanabilirler. Customer Insights'ın Retail ile tümleştirilmesi, perakendecilerin müşteri defterindeki müşteri kartında gösterilmesi gereken bir veya daha fazla ölçümü seçmelerine olanak tanır. Örneğin, perakendeciler bir müşteri için "kayıp olasılığını" hesaplamak ve "sonraki en iyi eylemi" tanımlamak için Customer Insights'taki verileri kullanabilir. Bu değerler ölçüm olarak tanımlanırsa müşteri kartında gösterilebilir ve satış yetkililerine önemli bilgiler sağlayabilir. Customer Insights hakkında daha fazla bilgi için [Dynamics 365 Customer Insights](https://docs.microsoft.com/dynamics365/ai/customer-insights/overview) belgelerine bakın. Ölçümler hakkında daha fazla bilgi için bkz. [Ölçümler](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="set-up-clienteling"></a>Müşteri rehberliğini ayarlama

Ortamınızda müşteri rehberliği işlevini açmak için aşağıdaki adımları izleyin.

1. **Özellik yönetimi** çalışma alanında, özellikleri **Perakende ve ticaret** modülüne göre filtreleyin.

    ![Perakende ve ticaret modülü için özellikler listesinde müşteri rehberliği](./media/Enable_clienteling.png "Perakende ve ticaret modülü için özellikler listesinde müşteri rehberliği")

2. **Şimdi etkinleştir** öğesini seçerek **Müşteri rehberliği** özelliğini açın.
3. **Perakende Parametreleri** sayfasında, **Numara serisi** sekmesinde, **Müşteri defteri tanımlayıcısı** satırını seçin. Ardından **Numara serisi kodu** alanından bir numara serisi seçin. Sistem, bu numara serisini müşteri defterlerine bir kod atamak için kullanır.
4. **Kaydet**'i seçin.
5. Müşteri defterlerinde yönetilen müşteriler için yakalamak istediğiniz öznitelikleri içeren yeni bir öznitelik grubu oluşturun. Yönergeler için bkz. [Öznitelikler ve öznitelik grupları](https://docs.microsoft.com/dynamics365/retail/attribute-attributegroups-lifecycle).

    - Gerekli öznitelikleri **İyileştirilebilir** olarak tanımlayın. Satış yetkilileri daha sonra bu öznitelikleri müşteri defterlerini filtrelemek için kullanabilir.
    - Bu öznitelikler için görüntüleme sırası ayarlayın. Bu görüntüleme sırası, müşteri defterindeki müşteri kartında hangi özniteliklerin gösterilmesi gerektiğini belirler. Görüntüleme sırası 1'in görüntüleme sırası 2'den yüksek olduğu kabul edilir. Bu nedenle, görüntüleme sırası 1 olan öznitelik, görüntüleme sırası 2 olan öznitelikten önce görüntülenir.

    > [!NOTE]
    > Customer Insights'ı aynı sayfadan kullanılabilir hale getirebilirsiniz. Ancak kimlik doğrulama amacıyla bir Azure uygulama kodu ve parola oluşturulmalıdır. (Gereksinimler hakkında bilgi için bu konunun ilerleyen bölümlerindeki [Customer Insights'ın Retail ile tümleştirilmesini açma](#turn-on-the-integration-of-customer-insights-with-retail) bölümüne bakın.) Customer Insights açıksa ve müşteri kartında gösterilmesi gereken bir veya daha fazla ölçümü seçtiyseniz bu ölçümler önce gösterilir. Ardından görüntüleme sırasına göre müşteri defteri öznitelik grupları gösterilir. Örneğin, Customer Insights'tan iki ölçüm seçerseniz müşteri kartında bu iki ölçüm ve bir müşteri defteri özniteliği gösterilir. (Gösterilen müşteri defteri özniteliği, en yüksek görüntüleme sırasına sahip özniteliktir.)

6. **Perakende parametreleri** sayfasında, **Müşteri rehberliği** sekmesinde, **Müşteri defteri öznitelik grubu** alanında, oluşturduğunuz öznitelik grubunu seçin.

    ![Seçilen müşteri defteri öznitelik grubu](./media/Client%20book%20attributes.png "Seçilen müşteri defteri öznitelik grubu")

7. POS'ta gerçekleşen faaliyetleri yakalamak için **Faaliyet türleri** sayfasında (**Perakende \> Müşteriler \> Faaliyet türleri**) faaliyet türlerini tanımlayın.

    > [!NOTE]
    > Faaliyet türleri, gerçek zamanlı arama ilk yapıldığında Retail Server tarafından çekilir. Faaliyetler çekildikten sonra birkaç saatliğine önbelleğe alınır. Faaliyet türlerini değiştirirseniz önbellek artık geçerli olmayana kadar bekleyin. Alternatif olarak, üretim dışı ortamlarda Retail Server hizmetini yeniden başlatın.

8. Satış yetkililerinin kendi müşteri defterlerini ve mağaza müşteri defterlerini görüntüleyebilmeleri için uygun POS ekranı düzenine iki düğme ekleyin. (Mağaza müşteri defterleri, bir adres defterini mağaza ile paylaşan tüm yetkililerin tüm müşteri defterlerindeki müşterileri içerir.) Karşılık gelen işlemler sırasıyla **Müşteri defterinde müşterileri görüntüle** ve **Mağaza müşteri defterlerinde müşterileri görüntüle** olarak adlandırılır. Müşteri defterleriyle ilgili üç ek işlem kullanılabilir. Bu işlemler, hangi yetkililerin müşteri defterinden müşteri ekleyebileceğini, kaldırabileceğini ve yeniden atayabileceğini belirler. Bunlar sırasıyla **Müşteriyi müşteri defterine ekle**, **Müşterileri müşteri defterinden kaldır** ve **Müşterileri müşteri defterine yeniden ata** olarak adlandırılır.
9. Aşağıdaki dağıtım planı işlerini çalıştırın: 1040, 1150, 1110 ve 1090.

Bu yordamı tamamladıktan sonra, satış yetkilileri POS'ta müşteri ayrıntıları sayfasını açabilir ve müşteri defterlerine müşteriler ekleyebilir, müşteriler için faaliyetleri ve notları görüntüleyip yakalayabilir ve müşteri defterini filtrelemek için müşteri ve müşteri defteri özniteliklerini kullanarak müşterileri hedefleyebilir. Aşağıdaki şekilde bir müşteri defteri örneği gösterilmiştir.

![Müşteri defteri örneği](./media/client_book.png "Müşteri defteri örneği")

## <a name="turn-on-the-integration-of-customer-insights-with-retail"></a>Customer Insights'ın Retail ile tümleştirilmesini açma

Customer Insights'ın Retail ile tümleştirilmesini açmak için Retail'in kullanıldığı kiracıda etkin bir Customer Insights kurulumunuzun olduğundan emin olmanız gerekir. Ayrıca Azure aboneliğinin bulunduğu bir Azure Active Directory (Azure AD) kullanıcı hesabınızın olması gerekir.

Tümleştirmeyi ayarlamak için aşağıdaki adımları izleyin.

1. Azure portalında, bir uygulama kaydedin. Bu uygulama, Customer Insights'ta kimlik doğrulama için kullanılır. Yönergeler için bkz. [Hızlı Başlangıç: Microsoft kimlik platformu ile bir uygulamayı kaydetme](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).
2. Uygulama için bir parola oluşturun. Daha sonra ihtiyacınız olacağından parolayı not edin ve güvenli bir yerde saklayın. Parola için bitiş süresi de seçin.

    > [!IMPORTANT]
    > Süresi dolmadan parolayı değiştirdiğinizde anımsayabilmenizi sağlayacak adımları atın. Aksi takdirde, tümleştirme beklenmedik şekilde durdurulur.

3. Azure anahtar kasası oluşturun ve uygulama parolasını kaydedin. Yönergeler için bkz. [Hızlı Başlangıç: Azure portalını kullanarak Azure Anahtar Kasasında bir parola ayarlama ve alma](https://docs.microsoft.com/azure/key-vault/quick-create-portal).
4. Retail'de Azure Anahtar Kasasına erişimi açın. Bu adımı tamamlamak için uygulama kodu ve parolanızın olması gerekir. Uygulama, 1. adımda oluşturduğunuz uygulamayla aynı veya yeni bir uygulama olabilir. (Başka bir deyişle, 1. adımda oluşturduğunuz uygulamayı Anahtar Kasası erişimi ve Customer Insights hizmeti erişimi için kullanabilir veya her erişim türü için benzersiz bir uygulama oluşturabilirsiniz.) Yönergeler için bkz. [Azure Yığını Anahtar Kasasında hizmet sorumlusu kimlik bilgilerini depolama](https://docs.microsoft.com/azure-stack/user/azure-stack-key-vault-store-credentials?view=azs-1908#create-a-service-principal).
5. Retail Headquarters'ta, **Sistem yönetimi \> Ayar \> Anahtar Kasası parametreleri**'ne gidin ve anahtar kasası için gerekli bilgileri girin. Ardından Retail'in anahtar kasasındaki parolalara erişebilmesi için **Anahtar Kasası istemcisi** alanına, 4. adımda kullandığınız uygulama kodunu girin.
6. 1. adımda oluşturduğunuz uygulamayı güvenli uygulamalar listesine (bazen beyaz liste olarak adlandırılır) eklemek için Customer Insights'a gidin ve uygulamaya **Görüntüleme** erişimi sağlayın. Yönergeler için bkz. [İzinler](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-permissions).
7. Retail'de, **Perakende parametreleri** sayfasında, **Müşteri rehberliği** sekmesinde, **Dynamics 365 Customer Insights** hızlı sekmesinde aşağıdaki adımları izleyin:

    1. **Uygulama Kodu** alanına, 1. adımda kullandığınız uygulama kodunu girin.
    2. **Parola adı** alanına, 5. adımda oluşturduğunuz Anahtar Kasası parolasının adını girin.
    3. **Customer Insights'ı etkinleştir** seçeneğini **Evet** olarak ayarlayın. Kurulum herhangi bir nedenle başarısız olursa bir hata iletisi alırsınız ve bu seçenek **Hayır** olarak ayarlanır.
    4. Customer Insights'ta test ve üretim ortamları gibi birden çok ortama sahip olabilirsiniz. **Ortam kurulumu kodu** alanına, uygun ortamı girin.
    5. **Alternatif müşteri kodu** alanına, Customer Insights'ta müşteri hesap numarasıyla eşleşen özelliği girin. (Retail'de müşteri hesap numarası müşteri kodudur.)
    6. Kalan üç özellik, müşteri defterindeki müşteri kartında gösterilecek ölçümlerdir. Müşteri kartında gösterilmek üzere en fazla üç ölçüm seçebilirsiniz. (Ancak herhangi bir ölçüm seçmeniz gerekmez.) Daha önce de belirtildiği gibi sistem önce bu değerleri ve ardından müşteri defteri öznitelik grubunun değerlerini gösterir.
