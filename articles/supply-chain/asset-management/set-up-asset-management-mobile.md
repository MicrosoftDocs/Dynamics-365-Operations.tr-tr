---
title: Kıymet yönetimi mobil çalışma alanını ayarlama
description: Bu makalede, çalışanların kıymet yönetimi görevlerini gerçekleştirmek üzere kullanabileceği bir Kıymet yönetimi mobil çalışma alanı çalıştırmak için Microsoft Dynamics 365 Supply Chain Management ve Finance and Operations (Dynamics 365) mobil uygulamasını ayarlama açıklanmaktadır.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ef4e6bf2ae59adb05c7d4aacc3f5675a5adcafc9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070068"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>Kıymet yönetimi mobil çalışma alanını ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, çalışanların kıymet yönetimi görevlerini gerçekleştirmek üzere kullanabileceği bir **Kıymet yönetimi** mobil çalışma alanı çalıştırmak için Microsoft Dynamics 365 Supply Chain Management ve Finance and Operations (Dynamics 365) mobil uygulamasını ayarlama açıklanmaktadır.

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Supply Chain Management'ta bakım görevlisi kullanıcılarını ayarlama

**Kıymet yönetimi** mobil çalışma alanına erişmesi gereken her bir kullanıcı için aşağıdaki adımları izleyin.

1. Supply Chain Management'ta **İnsan kaynakları \> Çalışanlar**'a gidin ve ayarlamak istediğiniz kullanıcı için bir çalışan kaydının olduğundan emin olun. Gerekirse yeni bir çalışan kaydı oluşturun.
1. **Kıymet yönetimi \> Kurulum \> Çalışanlar \> Çalışanlar**'a gidin ve önceki adımda tanımladığınız (veya oluşturduğunuz) çalışan kaydının bakım görevlisi kaydıyla eşleştiğinden emin olun. Gereken şekilde yeni bir bakım görevlisi kaydı oluşturun ve **Çalışan** alanını önceki adımdaki çalışan kaydı olarak ayarlayın.
1. **Kıymet yönetimi \> Kurulum \> Çalışanlar \> Bakım görevlisi grupları**'na gidin ve önceki adımda tanımladığınız (veya oluşturduğunuz) çalışan kaydının bakım görevlisi grubuna ait olduğundan emin olun.
1. **Sistem yönetimi \> Kullanıcılar**'a gidin.
1. Izgaradan ilgili kullanıcıyı seçin.
1. **Kullanıcı Ayrıntıları** hızlı sekmesinde, **Kişi** alanını geçerli kullanıcıyla eşleştirmek istediğiniz çalışan hesabına ayarlayın. Bu çalışan hesabı, 1. adımda tanımladığınız (veya oluşturduğunuz) çalışan kaydı olmalıdır ve 2. adımdaki bakım görevlisi kaydına eşlenmiş olmalıdır.

> [!NOTE]
> Kullanıcı izinleri ve güvenlik rolleri, Supply Chain Management kullanıcı arabiriminin özellikleri için geçerli oldukları gibi **Kıymet yönetimi** mobil çalışma alanının özellikleri için de geçerlidir. Bu nedenle, **Kıymet yönetimi** mobil çalışma alanına erişmek için ayarladığınız her kullanıcının Supply Chain Management'ta doğrudan benzer işlemleri gerçekleştirmek için gerekli güvenlik rollerine sahip olması gerekir.

## <a name="publish-the-asset-management-mobile-workspace"></a>Kıymet yönetimi mobil çalışma alanını yayımlama

Finance and Operations (Dynamics 365) mobil uygulamasında kıymet yönetimi özelliklerini kullanılabilir hale getirmek için **Kıymet yönetimi** mobil çalışma alanını yayımlamanız gerekir.

1. Supply Chain Management'ta **Ayarlar** düğmesini (sağ üst köşedeki dişli simgesi) seçin ve ardından menüdeki **Mobil uygulama**'yı seçin.
1. **Mobil uygulamayı yönet** iletişim kutusunda **Kıymet Yönetimi** kutucuğunu bulun. "Meta veride - yayımlanmadı" metnini içeriyorsa çalışma alanı henüz yayımlanmamıştır. "Meta veride - yayımlandı" metnini içeriyorsa çalışma alanı zaten yayımlanmıştır ve bu yordamın geri kalanını atlayabilirsiniz.

    ![Mobil uygulamayı yönet iletişim kutusu.](media/mobile-workspaces.png "Mobil uygulamayı yönet iletişim kutusu")

1. **Kıymet yönetimi** kutucuğunu seçin ve ardından araç çubuğunda **Yayımla**'yı seçin. Birkaç saniye sonra, çalışma alanının başarıyla yayımlandığını bildiren bir bildirim almalısınız. Ek olarak, kutucuktaki metin "Metaveride - yayımlandı" olarak değişmelidir.

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>Finance and Operations (Dynamics 365) mobil uygulamasını yükleyip ayarlama

1. Mobil cihazınıza **Microsoft Finance and Operations (Dynamics 365)** uygulamasını yüklemek için aşağıdaki uygulama mağazalarından birine gidin:

    - [Google Android cihazlar için](https://go.microsoft.com/fwlink/?linkid=850662)
    - [Apple iOS cihazlar için](https://go.microsoft.com/fwlink/?linkid=850663)

1. Finance and Operations (Dynamics 365) uygulamasını açın. Oturum açma sayfası görünmelidir. **Oturum açma** alanına, Supply Chain Management URL'nizi girin veya **Son ortamlar** listesinde son URL'yi seçin ve **Bağlan**'a dokunun.

    ![Oturum açma sayfası.](media/mobile-app-sign-in.png "Oturum açma sayfası")

1. Bağlantıyı onaylamanız istenirse **Anladım** onay kutusunu seçin ve ardından **Bağlan**'a dokunun.
1. **Bir hesap seçin** sayfasında, mobil uygulamada oturum açmak için Microsoft hesabınızı kullanın.

    **Çalışma alanları** sayfası görüntülenir. Supply Chain Management kurulumunuz tarafından yayımlanmış tüm mobil çalışma alanını listeler.

    ![Çalışma alanları listesi.](media/mobile-app-workspaces.png "Çalışma alanları listesi")

1. Tüzel kişiliği (şirket) değiştirmeniz gerekiyorsa sol üst köşedeki Menü düğmesine (bazen hamburger veya hamburger düğmesi olarak da adlandırılır) dokunun ve ardından **Şirketi değiştir**'e dokunun.

    ![Tüzel kişiliği değiştirme.](media/mobile-app-change-comp.png "Tüzel kişiliği değiştirme")

1. **Çalışma alanları** sayfasında, çalışmak istediğiniz çalışma alanını seçerek açın.

    ![Varlık yönetimi mobil çalışma alanı.](media/mobile-app-asset-workspace.png "Varlık yönetimi mobil çalışma alanı")

## <a name="work-with-the-asset-management-mobile-workspace"></a>Kıymet yönetimi mobil çalışma alanıyla çalışma

**Kıymet yönetimi** mobil çalışma alanıyla nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Kıymet yönetimi mobil çalışma alanını kullanma](asset-management-mobile-workspace.md).

Finance and Operations (Dynamics 365) mobil uygulaması hakkında daha fazla bilgi için bkz. [Mobil uygulama giriş sayfası](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
