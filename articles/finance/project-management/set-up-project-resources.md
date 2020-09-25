---
title: Proje kaynaklarını ayarlama
description: Bu konu, proje kaynaklarını ayarlama veya isteme hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760688"
---
# <a name="set-up-project-resources"></a>Proje kaynaklarını ayarlama

[!include [banner](../includes/banner.md)]

Bir takvim ayarlamanız ve bunu bir personel veya çalışanla ilişkilendirmeniz gerekir. Takvim, projeyi ve projeye rezerve edilen kaynakların çalışma zamanını planlamak için kullanılır. Takvim ayarlama işlemi sırasında, proje yöneticileri kaynak eşitlemeyi kaynak optimizasyonunun bir parçası olarak yapabilir. Takvim planına bağlı olarak, kaynaklara kısıtlamalar yerleştirebilir. **Takvimler** sayfasından bir takvim ayarlayabilirsiniz.

Bir proje kaynağı için bir çalışan ayarlarsanız, kaynağı ayarladığını şirkette çalışan çalışanlar arasından seçim yapabilirsiniz. Alternatif olarak, kuruluşunuzdaki diğer şirketlerden çalışanları seçebilirsiniz. Bu çalışanlar şirketlerarası kaynak olarak bilinir.

Aşağıdaki yordamlar bir çalışanı şirketinizdeki bir proje kaynağı olarak nasıl ayarlayacağınızı ve nasıl bir şirketlerarası proje kaynağı ayarlayabileceğinizi açıklamaktadır.

## <a name="set-up-a-worker-as-a-project-resource"></a>Bir çalışanı proje kaynağı olarak ayarlama

1. **Çalışanlar** sayfasındaki **Çalışanlar** listesinde proje kaynağı olarak eklediğiniz çalışanı seçin ve çalışan kaydını açın.
2. Eylem Bölmesinde **Proje** &gt; **Ayar** &gt; **Proje ayarı**'nı seçin.
3. Bir takvim seçin ve sayfayı kapatın.

Bir kaynak için ön atama türü olarak varsayılan projeleri de belirtebilirsiniz. Ön atamalar, kaynak yöneticisi veya proje yöneticisi, kaynağın hangi projede çalışacağını önceden bildiğinde kullanılır. Ön atamalar için bir proje sponsoru veya müşterinin talebi de temel alınabilir. Bir projeyi önceden atamak için **Projeleri ata** sayfasındaki **Projeler** sekmesinde bulunan **Kalan projeler** listesinden ilgili projeyi seçin.

## <a name="set-up-an-intercompany-resource"></a>Şirketlerarası bir kaynak ayarlama

Bir çalışanı şirketlerarası kaynak olarak ayarladığınızda, hem ayarı ödünç veren hem de ödünç alan şirkette tamamlamanız gerekir.

### <a name="in-the-lending-company"></a>Ödünç veren şirkette

1. Finance'te, borç veren şirketin seçildiğini doğruladıktan sonra, önceki bölümdeki "Bir çalışanı proje kaynağı olarak ayarlama" yordamını tamamlayın.
2. **Şirketlerarası muhasebe** sayfasında, **Yeni**'yi seçin.
3. **Tüzel kişilik kimliği** alanında, ödünç veren şirketi seçin. Kalan alanları uygun şekilde doldurun ve **Kaydet**'i seçin.
4. **Transfer fiyatı** sayfasında, **Yeni**'yi seçin.
5. **Ödünç alan tüzel kişilik** alanında, uygun şirketi seçin.
6. Ödünç alan şirkete bölümün başında oluşturulan kaynağı ödünç vermek için **Kaynak** alanında, oluşturduğunuz kaynak adını seçin. Şirketteki tüm kaynakları ödünç alan şirketin kullanımına sunmak için, **Kaynak** alanını boş bırakın.
7. **Proje yönetimi ve muhasebe parametreleri** sayfasında **Şirketlerarası** sekmesinde, **Şirketlerarası kaynak planlamayı ve zaman çizelgelerini etkinleştir** seçeneğini **Evet** olarak ayarlayın.

### <a name="in-the-borrowing-company"></a>Ödünç alan şirkette

- **Kaynak listesi** sayfasında arama filtresi alanına, ödünç alan şirketin kaynak listesine adın eklendiğini doğrulamak için ödünç veren şirket için oluşturduğunuz kaynağın adını girin.

## <a name="request-project-resources"></a>Proje kaynaklarını isteme
Proje kaynak planlama işlevselliği yalnızca kaynak yöneticilerinin personelleri kaynakları görevlere veya projelere dağıtmasını destekler. Bu işlevi etkinleştirmek için aşağıdaki görevleri tamamlayın veya bu görevlerin tamamlandığını doğrulayın:

- Numara serileri ayarlayın.
- Proje yönetimi ve muhasebe iş akışları ayarlayın.
- Kaynak isteği iş akışlarını etkinleştir.

Önceki görevler tamamlandıktan sonra, aşağıdaki görevleri istediğiniz gibi tamamlayabilirsiniz:

- Geçici rezervasyon personelli kaynağından bir kaynak isteği oluşturun.
- Kaynak isteklerini izleyin.
- Kaynak isteklerini karşılayın.
- WBS'den personelli bir kaynak isteyin.
- Personelli kaynak isteği olmayan bir projeye kaynaklar rezerve edin.
