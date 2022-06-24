---
title: Mobil cihaz kullanıcı hesapları
description: Bu makalede, çalışanların oturum açmasına ve ambar uygulamasını kullanmasına olanak tanıyan kullanıcı hesaplarının nasıl ayarlanacağı ve yönetileceği açıklanmaktadır.
author: Mirzaab
ms.date: 09/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ffb4a9842f454094b41a1765d1438f6a40ae610b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851318"
---
# <a name="mobile-device-user-accounts"></a>Mobil cihaz kullanıcı hesapları

[!include [banner](../includes/banner.md)]

Bir çalışan ambar uygulamasını kullanmaya her başladığında, bir kullanıcı adı ve parola kullanarak oturum açmaları gerekir. Ambar uygulaması kullanıcıları, sistemdeki her bir çalışan ile ilişkilendirilebilir ve ambarlar genellikle bu ambar uygulama kullanıcılarından her biriyle ilişkilendirilir. Ayrıca, ambar uygulamasını kullanmayla ilgili varsayılan ayarları ve diğer ayarları oluşturmak üzere her çalışan için çeşitli seçenekler konfigüre edilir.

## <a name="set-up-the-required-worker-and-employee-records"></a>Gerekli çalışan ve çalışan kayıtlarını ayarlama

Ambar uygulama kullanıcılarını ayarlamadan önce, her çalışanın **İnsan Kaynakları** modülünde Supply Chain Management çalışanı veya çalışan olarak zaten mevcut olması gerekir.

## <a name="set-up-mobile-device-user-accounts"></a><a name="set-wma-users"></a>Mobil cihaz kullanıcı hesapları ayarlama

Gerekli çalışan ve çalışanlar İnsan Kaynaklarında oluşturulduktan sonra, her birine ambar uygulama kullanıcıları atayabilir ve bu uygulamayı nasıl kullanabileceğinizi etkileyen diğer seçenekleri ayarlayabilirsiniz.

1. **Ambar yönetimi \> Kurulum \> Çalışan**'a gidin.
1. Varolan bir çalışanı düzenlemek için, birimi liste bölmesinde seçin. Yeni bir kayıt eklemek için Eylem Bölmesinde **Yeni**'yi seçin.
1. Yeni bir çalışan ayarlıyorsanız, şu adımları izleyin:

    1. **Çalışan** alanında, personel listesinden hedef kullanıcıyı seçin.
    1. **Seç** öğesini seçin.
    1. Eylem bölmesinde, **Kaydet**'i seçin.

1. Varsayılan bir profil, ambar çalışanına, burada gerekli olan işlem aracılığıyla ambalaj istasyonundan kılavuzluk etmek için kullanılabilir. Alternatif olarak, çalışanın tercih edilen profil ayarlarını kaydetmek için varsayılan profil kullanılabilir. **Profil** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Konteyner paketleme ilkesi** – Paketleme istasyonunda kapsayıcıların nasıl işlenmesi gerektiğini tanımlayan bir konteyner ambalaj ilkesi seçin. Burada seçilen konteyner ambalaj ilkesi, ambalaj istasyonunu açtıklarında çalışan için önceden seçilmiş olacaktır. Daha fazla bilgi için aşağıdaki blog gönderisine bakın: [İyileştirilmiş paketleme işlevi](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611),
    - **Paketleme profili kodu** – Kullanılan paketleme ilkesi ve konteyner ayarlarını tanımlayan bir ambalaj profili kodu seçin. Seçilen ambalaj profili kodu bir konteyner ambalaj ilkesiyle ilişkilendirilmişse, bu sayfadaki **Konteyner ambalaj ilkesi** ayarını değiştiremezsiniz.

1. **Varsayılan ambalaj istasyonu** hızlı sekmesinde, alt öğe oturum açtığında geçerli olan varsayılan ambalaj istasyonunu tanımlamak için aşağıdaki alanları ayarlayın. Çalışan, gerekirse hâlâ başka bir ambalaj istasyonunu seçebilir.

    - **Site** – Varsayılan ambalaj istasyonunun bulunduğu siteyi seçin.
    - **Ambar** – Varsayılan ambalaj istasyonunun bulunduğu ambarı seçin.
    - **Yerleşim** – Varsayılan ambalaj istasyonunun konumunu seçin.

1. **Kullanıcılar** hızlı sekmesi, seçilen çalışan için istediğiniz sayıda ambar uygulama kullanıcı hesabı oluşturmanıza olanak tanır. Her hesap belirli bir ambar veya ambarlarla ilişkilendirilir. Kullanıcı hesabı eklemek veya kaldırmak, seçili bir hesabın parolasını sıfırlamak veya seçili bir hesaba ambar atamak için araç çubuğunu kullanın. Her kullanıcı hesabı için aşağıdaki alanları ayarlayın:

    - **Kullanıcı Kimliği** – Benzersiz bir kimlik girin.
    - **Kullanıcı adı** – Kimlik için bir ad girin.
    - **Varsayılan ambar** – Çalışanın genellikle çalıştığı varsayılan ambarı ayarlayın. Ek ambarlar atamak için araç çubuğunu kullanabilirsiniz ve mobil aygıt menü öğesinin **Ambarı değiştir** dolaylı faaliyetini kullanarak, çalışan ambarlar arasında geçiş yapabilirsiniz.
    - **Menü adı** – Çalışanın başlangıç sayfası olacak kök menüyü seçin. Her çalışan için bir kök menüsü kurma yeteneği, her çalışanın kullanabileceği menü yapısını denetlemenize olanak sağladığından yararlıdır. Örneğin, yalnızca çıkış alanında etkin olan çalışanlar için olan menü, o alanın giden operasyonlarla ilgili görevler için ayarlanabilir.
    - **Etkin değil** – Seçili bir onay kutusu, kullanıcı hesabının etkin olmadığını belirtir. Bir çalışan ambar uygulamasının bir satırına beş kez yanlış parola girerse, kullanıcı hesabı otomatik olarak devre dışı bırakılır. Ancak bu onay kutusunu el ile de seçebilirsiniz. Kullanıcıyı yeniden etkin hale getirmek için onay kutusunu temizleyin.

1. **Çalışma** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Çekme konumu geçersiz kılmaya izin ver** – Çalışanın malzeme çekme adımlarının konumunu geçersiz kılmasına izin vermek için bu seçeneği *Evet* olarak ayarlayın. Fiziksel stok, sistem tarafından önerilen konumla eşleşmezse bu yetenek kullanışlı olabilir.
    - **Koyma konumu geçersiz kılmaya izin ver** – Çalışanın koyma adımlarının konumunu geçersiz kılmasına izin vermek için bu seçeneği *Evet* olarak ayarlayın. Önerilen koyma konumu zaten dolu veya kullanılamıyorsa ya da hazırlama yerleşimleri değiştirilirse bu yetenek yararlı olabilir.
    - **Malzeme çekme üzerinden satışlara izin ver** – Satış siparişleri çekildiğinde çalışanın aşırı çekmesine izin vermek için bu seçeneği *Evet* olarak ayarlayın. Daha fazla bilgi için bkz. [Satış siparişleri ve transfer emirleri için fazla malzeme çekme](over-picking-for-sales-and-transfer-orders.md).
    - **Malzeme çekme üzerinden transfer siparişi** – Transfer siparişleri çekildiğinde çalışanın aşırı çekmesine izin vermek için bu seçeneği *Evet* olarak ayarlayın. Daha fazla bilgi için bkz. [Satış siparişleri ve transfer emirleri için fazla malzeme çekme](over-picking-for-sales-and-transfer-orders.md).
    - **İlişkili işle stok hareketine izin ver** – Çalışanın zaten rezerve edilmiş veya zaten başka bir çalışmayla ilişkilendirilmiş stoğu taşımasına izin vermek için bu seçeneği *Evet* olarak ayarlayın. Daha fazla bilgi için bkz. [Ambar yönetiminde stoku ilişkili işle birlikte taşıma](move-inventory-associated-work.md).
    - **El ile madde tahsisatı yapılmasına izin ver** – Kısa çekme sırasında çalışan için el ile yeniden tahsisat özelliğini etkinleştirmek üzere bu seçeneği *Evet* olarak ayarlayın. Madde yeniden tahsisatı, çalışanların başka bir konumdan stok çekmesini sağlar. Tüm çalışanlar için otomatik yeniden tahsisat kullanılabilir olmakla birlikte, el ile yeniden tahsisat bir çalışan için açık olarak kurulmalıdır. Her bir çalışanın el ile yeniden tahsisat işlemini denetleme yeteneği yararlı olabilir, çünkü örneğin karantinadan veya toplu alandan alınan madde çekme güvenilen çalışanlara sınırlı olduğunda her çalışanın görünürlüğünü kontrol etmenizi sağlar. Daha fazla bilgi için aşağıdaki blog gönderisine bakın: [Kısa malzeme çekme sırasında otomatik ve el ile madde yeniden tahsisatı](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/11/07/automatic-and-manual-item-reallocation-during-the-short-picking-dynamics-365-for-operations-1611/).
    - **Döngü sayısı gözetmeni** – Bir çalışanı, alt döngü sayımı gözetmeni olarak belirlemek için bu seçeneği *Evet* olarak ayarlayın. Bu durumda, çalışanın ambar uygulaması üzerinde gerçekleştirdiği tüm döngü sayımları hemen onaylanır. Bu seçeneğin *Evet* olarak ayarlandığı çalışanlar için **Maksimum yüzde sınırı**, **Maksimum miktar sınırı** ve **Maksimum değer sınırı** alanları dikkate alınmaz.
    - **Maksimum yüzde sınırı** – Döngü sayısı yöneticisi tarafından onayı gerektirmeden bir döngü sayısının beklenen sayıdan farklı olabileceği en yüksek yüzde sınırını girin.
    - **Maksimum miktar limiti** – Bir döngü sayısı amiri tarafından onay gerektirmeden, girilen miktarın beklenen miktardan (birim cinsinden) farklı olabileceği toplam miktarı girin.
    - **Maksimum değer sınırı** – Döngü sayısı yöneticisi tarafından onayı gerektirmeden stok maliyetinin beklenen maliyetten farklı olabileceği maksimum tutarı girin.

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Yeni bir kullanıcı hesabı eklediyseniz, **Parola ayarla** iletişim kutusu görüntülenir; bu iletişim kutusunda kullanıcının mobil uygulamada oturum açmak için kullanabileceği basit bir parola oluşturabilirsiniz. Basit parolayı iki kez girin ve sonra devam etmek için **Parolayı kaydet**'i seçin.

## <a name="set-the-language-number-formats-and-time-zone-for-each-warehouse-app-user"></a>Her ambar uygulama kullanıcısı için dil, sayı biçimi ve saat dilimini ayarlayın

Warehouse Management mobil uygulamasında bir çalışan oturum açtığında, dil, sayı biçimleri ve saat dilimi, çalışanın tercihlerine uyacak şekilde değişecektir. [Mobil aygıt kullanıcı hesaplarını ayarla](#set-wma-users) bölümündeki 3 numaralı adımda seçilen çalışan için hesap ayarları, kullanılan ayarları belirler. Her bir kullanıcı için ayrı ayarlar gerekiyorsa, farklı çalışan hesapları kullanın. Aşağıdaki yordamda, her ambar uygulama kullanıcısı için dilin, sayı biçimlerinin ve saat diliminin nasıl değiştirileceği gösterilmektedir.

1. **Ambar yönetimi \> Kurulum \> Çalışan**'a gidin.
1. Ayarlamak istediğiniz çalışanın adını bulun. Çalışanın, **Kullanıcılar** hızlı sekmesinde listelenmiş gerekli tüm ambar uygulama kullanıcı hesaplarına sahip olduğundan emin olun. [Mobil aygıt kullanıcı hesaplarını ayarla](#set-wma-users) bölümündeki adımları izleyerek gerektiği şekilde yeni bir çalışan oluşturun ve/veya ambar uygulaması kullanıcı hesaplarını ekleyin.
1. **Sistem yönetimi \> Kullanıcılar \> Kullanıcılar**'a gidin.
1. **Kişi** sütununda, adım 2'de bulunan çalışanın adını gösteren kullanıcı hesabını seçin.

    > [!IMPORTANT]
    > **Kullanıcılar** sayfasında listelenen **Kullanıcı kimliği** değerleri, adım 1'de açtığınız **Çalışan** sayfasının **Kullanıcılar** hızlı sekmesinde gösterilen değerle ilişkili *değildir*.

1. Eylem Bölmesinde, **Kullanıcı seçenekleri**'ni seçin.
1. **Tercihler** sekmesinde, aşağıdaki alanları ayarlayın:

    - **Dil** – Çalışanın tercih ettiği dili seçin. Bu alan aynı zamanda ambar uygulamasında gösterilen sayı biçimini de denetler.
    - **Tarih, saat ve sayı biçimi**: Çalışanın tercih ettiği tarih ve saat biçimini seçin. Ambar uygulamasında bu ayar yerine **Dil** alanında seçilen dille ilişkili sayı biçimi kullanılır.
    - **Saat dilimi** – Çalışanın çalıştığı saat dilimini seçin. Bu alan, uygulamayı kullanarak çalışanın yaptığı tüm kayıtlar için zaman damgasını etkiler.

> [!NOTE]
> Bazı durumlarda, ambar uygulaması dili, sayı biçimlerini ve saat dilimini oluşturan belirli çalışan ayarlarını bulamaz. Geçerli olan kurallar şunlardır:
>
> - Uygulama bir Supply Chain Management ortamına bağlı değilse (örneğin, uygulamayı yüklendikten sonra ilk kez başlatıldığında), yerel aygıtın dili kullanılır. Aygıt dili değiştiğinde, uygulama dili de değişir. Yerel aygıt dilini konfigüre etme hakkında daha fazla bilgi için, aygıtınızın ve/veya işletim sisteminizin belgelerine bakın.
> - Uygulama bir Supply Chain Management ortamına bağlıysa, ancak oturum açan çalışan için hiçbir tercih ayarlanmamışsa, aygıtın Supply Chain Management'a bağlanmak için kullandığı istemci kimliğiyle ilişkilendirilmiş hesaba dayalı olarak dil, sayı biçimleri ve saat dilimi seçilir. Daha fazla bilgi için bkz. [Supply Chain Management içinde bir kullanıcı hesabı oluşturma ve yapılandırma](install-configure-warehouse-management-app.md#user-azure-ad).

> [!TIP]
> Ambar uygulaması kullanılarak yapılan kayıtlar için yanlış zaman damgaları gösterileceğini fark ederseniz, çalışanların oturum açmak ve/veya Supply Chain Management ile kimlik doğrulamak için kullandığı kullanıcı hesabı için ayarlanan saat dilimini ayarlamanız gerekebilir. Daha önce belirtildiği gibi saat dilimi ayarı, **Çalışan** sayfasında ayarlandığı şekilde ambar uygulamasına oturum açmak için kullanılan kullanıcı hesabından gelebilir. Alternatif olarak, **Çalışan** sayfasında kullanıcı hesabı ayarlanmamışsa, saat dilimi, **[Azure Active Directory uygulamalar](install-configure-warehouse-management-app.md)** sayfasında ayarlandığı şekilde, kimlik doğrulama için kullanılan istemci kimliğiyle ilişkilendirilmiş kullanıcı hesabından gelir.
