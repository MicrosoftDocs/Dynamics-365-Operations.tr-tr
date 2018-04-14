---
title: "Microsoft Dynamics 365 for Talent işlevselliğini genişletme"
description: "Herhangi bir Microsoft PowerApps oluşturduysanız, bu uygulamaları Microsoft Dynamics 365 for Talent içindeki bağlantılardan başlatabilirsiniz."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 51eb4288f5b6c732755007c1dcd8c4db090ccc0a
ms.contentlocale: tr-tr
ms.lasthandoff: 03/08/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent işlevselliğini genişletme

[!INCLUDE [banner](includes/banner.md)]

Herhangi bir Microsoft PowerApps oluşturduysanız, bu uygulamaları Microsoft Dynamics 365 for Talent içindeki bağlantılardan başlatabilirsiniz. Uygulamalarınıza erişim ayarlamak için, Talent içinde bazı bilgileri **Sistem yönetimi** çalışma alanından açabileceğiniz bir yapılandırma sayfasında ayarlamanız gerekir.

## <a name="configuring-embedded-powerapps-within-talent"></a>Talent içinde katıştırılmış PowerApps yapılandırma
PowerApps uygulamalarını başlatmak üzere Talent sayfalarını yapılandırmak için **Katıştırılmış Microsoft PowerApps ayarlama** sayfasını kullanın. **Katıştırılmış Microsoft PowerApps ayarlama** sayfasını açmak için, **Sistem yönetimi** çalışma alanını ve ardından **Bağlantılar** sekmesini açın. **Kurulum** grubundan **Microsoft PowerApps**'i seçin. 

Aşağıdaki bilgileri bu sayfadan girilir veya ayarlanır: 

> - Her PowerApps uygulaması için açıklayıcı bir ad veya bir tanımlayıcı.
> - Talent sayfasına eklediğiniz her uygulama için benzersiz bir tanımlayıcı (GUID). Uygulama kodu PowerApps sitesinde bulunur, [powerapps.com](http://powerapps.com/). 
> - Kullanıcıların bir uygulama veya rapor açabilecekleri sayfa. Tüm Talent sayfaları katıştırılmış PowerApps'i ve Power BI raporlarını desteklemez. 
> 
> [!NOTE]
>  Sayfanın üstünde görüntülenen görünen ad yerine sayfanın dahili adını girin. Dahili adı bulmak için, adını öğrenmek istediğiniz sayfası açın ve sayfada herhangi bir yere sağ tıklayın. Menü açıldığında, **Form bilgileri** öğesinin üzerine gidin. Dahili form adı menüdeki **Form bilgileri** öğesinin yanında görüntülenir.
> 
> - Uygulamanın bağlam verilerini alabileceği form denetimini belirtin. Örneğin, bir uygulama bir çalışan hakkındaki verileri kullanabilir. **Bağlam** alanındaki **Çalışan** sayfasına girerseniz, **Çalışan** sayfası uygulamayı başlattığınızda açılır. **Bağlam alanındaki** bir giriş isteğe bağlıdır. 
> - PowerApps uygulamasının çalıştırılacağı iletişim kutusunun boyutunu ayarlayın. İletişim kutuları, uygulamanız bir telefonda veya geniş bir cihazda çalıştığında kullanıcı arabirimini en iyi duruma getirmek için sırasıyla "küçük" veya "büyük" olarak belirlenebilir. 

Ayrıca bir uygulamanın hangi tüzel kişilikler tarafından kullanılabileceğini belirleyebilir veya uygulamanın tüm tüzel kişilikler tarafından kullanılabilmesini sağlayabilirsiniz. Varsayılan olarak, PowerApps uygulamalarınız tüm tüzel kişiliklerin kullanımına sunulur.

## <a name="opening-an-application"></a>Uygulama açma
Katıştırılmış PowerApps uygulamaları yapılandırdığınızda, belirttiğiniz uygulama bağlantıları Talent içindeki sayfalara eklenir. Bir uygulamayı açmak için bir bağlantıya tıklayın. 



