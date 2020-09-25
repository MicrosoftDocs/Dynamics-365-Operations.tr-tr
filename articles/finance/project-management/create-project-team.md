---
title: Proje ekibi oluşturma
description: Bu konuda bir proje ekibi oluşturma ve yönetme hakkında bilgiler yer alır.
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
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760684"
---
# <a name="create-a-project-team"></a>Proje ekibi oluşturma

[!include [banner](../includes/banner.md)]

Bir projedeki önceden ayarlanmış olan rolleri kullanmak için bir proje yöneticisinin rolleri projeyle ilişkilendirmesi gerekir. Bir proje için birden fazla rol atanabilir. Karışıklığı önlemek için bu roller, rezervasyon sırasında otomatik etiketlenir. Örneğin, proje yöneticisi üç yazılım mühendisi istiyorsa, **yazılım mühendisi 1**, **yazılım mühendisi 2** ve **yazılım mühendisi 3** etiketlerine sahip üç Yazılım mühendisi rolü otomatik olarak oluşturulur. Rol için rol özellikleri önceden ayarlanmışsa, kaynak arama sırasında filtre olarak uygulanır. Aramayı daha detaylı hale getirmek için ek özellikler eklenebilir.

Kaynak kullanılabilirliğinin daha iyi görüntülenebilmesi için görüntüleme ayarları özelleştirilebilir. Saatlik, günlük, haftalık, aylık, üç aylık ve yıllık kullanılabilirliği gösterme seçenekleri vardır. Ayrıca, kullanılabilir ve kalan kaynak kapasitesini görüntüleme seçeneği de bulunur. Bu seçenek, faaliyetler veya kaynak kullanılabilirliği için kullanılabilir zamanı tahmin etmeniz gerektiğinde yararlıdır.

Proje yöneticisi sayfadan bir rol seçebilir ve gereksinimi karşılayan kullanılabilir bir kaynak varsa, rolü doldurmak için bir kaynak rezerve etmeyi seçebilir. Kaynakların, planlama aşamasının bu noktasında rezerve edilmemesi gerektiğini unutmayın. Bir WBS oluşturduğunuzda, rolleri projedeki personelli kaynaklarla değiştirebilirsiniz. Roller, WBS'deki personelli kaynaklarla değiştirilirse, kaynak ayarı proje ekibi listesini ve planlamasını otomatik olarak güncelleştirir.

[![Hem rolleri hem de gerçek kaynakları içeren proje ekibi listesi](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Proje yöneticisinin bir proje için bir kaynağı rezerve etmek için kullanabileceği **Kalan kapasite**, **Tam kapasite**, **Kapasite yüzdesi** ve **Saatleri belirtme** gibi çeşitli seçenekleri vardır. Kaynak atamalarını değiştirirseniz, bu rezerve etme seçenekleri herhangi bir zamanda iptal edilebilir. İki tür rezervasyon desteklenir:

- **Kesin Rezervasyon** – Kaynak rezervasyonu onaylanmış ve belirtilen süre için görevde çalışmak üzere doğrulanmıştır.
- **Geçici Rezervasyon** – Kaynak rezervasyonları geçici olarak belirtilen süre için görevde çalışmak üzere ayarlanmıştır.

Aşağıdaki yordamda bir proje ekibinin nasıl oluşturulacağı açıklanmaktadır.

## <a name="create-a-project-team"></a>Proje ekibi oluşturma

1. **Tüm projeler** liste sayfasında bir proje seçin ve ardından **Düzenle**'yi seçin.
2. **Proje ekibi ve planlama** sekmesindeki **Bitiş tarihini planla** alanına, planlanan başlama tarihi artı bir ay girin. Örneğin, planlama başlangıç tarihi 24 Haziran 2017 ise (24/06/2017), **24/07/2017** girin.
3. **Ekle**'yi seçin.
4. **Projeye roller ekle** bölmesindeki **Rol** alanında **Kıdemli Proje Yöneticisi**'ni seçin.
5. **Gerekli yetkinlikler**'i seçin.
6. **Özelliklerini seçin** sayfasında, Kıdemli proje yöneticisi rolü için önceden ayarlamış olduğunuz özellikler varsayılan olarak seçilir. **Tamam**'ı seçin.
7. **Projeye roller ekle** sayfasındaki **Kaynak sayısı** alanına **1** girin.
8. **Kaynak** alanında, arama gerekli yetkinliklere sahip tüm kaynakları gösterir. **Daniel Goldschmidt**'i seçin ve **Oluştur**'u seçin.
9. **Proje** sayfasında **Ekle**'yi seçin.
10. **Projeye roller ekle** bölmesindeki **Rol** alanında **Ekip üyesi**'ni seçin. **Kaynak sayısı** alanına **5** girin.
11. **Oluştur**'u seçin.
12. **Projeler** sayfasında **Kaynağı karşıla**'yı seçin.

## <a name="monitor-project-teams"></a>Proje ekiplerini izleme
1. **Tüm projeler** sayfasında **XYZ Yükseltme Aşama 2** projesi için **Proje kimliği** bağlantısına tıklayın.
2. **Proje ekibi ve planlama** hızlı sekmesinde, listelenen proje kaynaklarının doğru olduğunu kontrol edin.
