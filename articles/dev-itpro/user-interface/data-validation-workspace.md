---
title: "Veri doğrulama çalışma alanı"
description: "Veri doğrulama yapılacaklar listesi çalışma alanı, şirketler, bölgeler ve kişiler arasındaki veri doğrulama işlemlerini izlemenize olanak sağlar. Denetim listesi yeni bir uygulama sırasında, bir yükseltmeden sonra veya bir geçişten sonra kullanılabilir."
author: bking
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: bking
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 447fd87cb2f71147d7a9f6476f4ed9e12d75640a
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="data-validation-workspace"></a>Veri doğrulama çalışma alanı

[!include[banner](../includes/banner.md)]


Bu konu, **Veri doğrulama denetim listesi** çalışma alanı ve bununla ilişkili yapılandırma hakkında genel bir bakış sağlar.

## <a name="data-validation-checklist-workspace"></a>Veri doğrulama denetim listesi çalışma alanı

**Veri doğrulama yapılacaklar listesi** çalışma alanı, şirketler, bölgeler ve kişiler arasındaki veri doğrulama işlemlerini izlemenize olanak sağlar. Denetim listesi yeni bir uygulama sırasında, bir yükseltmeden sonra veya bir geçişten sonra kullanılabilir. **Veri doğrulama yapılacaklar listesi** çalışma alanınızın görünümüne bağlı olarak, bir veri doğrulama projesi için tüm görevleri ve durumlar ya da sadece size atanmış olan görevleri görürsünüz.

Önce çalışma alanının üstünden bir veri doğrulama projesi seçmelisiniz. Çalışma alanında gösterilen tüm veriler daha sonra seçilen veri doğrulama projesi ile filtrelenir.

### <a name="summary-tiles"></a>Özet kutucukları

**Özet** kutucukları işleme genel bir bakış sağlar ve veri doğrulama işleminin yolunda gittiğinden emin olmanızı sağlar. Kalan tüm görevleri, tamamlanan görevleri, süren görevleri ve işlem için başlatılmamış görevleri görürsünüz. Bu bilgi, seçilen veri doğrulama projesine dahil tüm şirketler için geçerlidir.

### <a name="tasks-and-status-section"></a>Görevler ve durum bölümü

**Görevler ve durum** bölümünde, veri doğrulama projesinin genel durumu çeşitli şekillerde görüntülenir: tüzel kişiliğe göre, bölgeye göre ve görev listesine göre durum. Ayrıca, belirli bir şirketin durumunu görüntülemek için filtre de seçebilirsiniz. Her durum sekmesi, hem tamamlanmış olan yüzde hem de kalan görevlerin sayısı hakkında bir çözümleme sağlar.

Son sekme, ayrıntılı görev listesi içindir. Bu liste, tam görev listesini gösterir.
Görev listesini çeşitli şekillerde filtrelenebilir. Görevin durumunu değiştirmek veya bir görev atamak için **Görevi düzenle**'ye tıklayın. Görevin eklerini görüntülemek için **Ekler** üzerine tıklayın.

Görev adı, kullanıcının görevi tamamlamak için gitmesi gereken Microsoft Dynamics 365 for Finance and Operations, Enterprise edition sayfasına giden bir köprüdür. Bu bağlantıyı, görevi **Veri yapılandırma projesi** formundan oluşturduğunuzda veya düzenlediğinizde **Menü öğesi adı** alanını kullanarak ayarlayabilirsiniz.

Dosyalar, notlar, resimler veya URL'leri bir göreve **Ekler** eylemini kullanarak ekleyebilirsiniz. Örneğin, bir görev için yazdırılan rapor dosyasını ekleyebilirsiniz. Bir ek mevcutsa, **Ek** sütununda bir simge belirir.

**Tarafından tamamlandı** seçeneği, görev tamamlandıktan sonra, görevi tamamlayan çalışanın adıyla otomatik doldurulacaktır. Bir görev, tamamlandı olarak işaretlendiğinde, **Tamamlandı tarihi** alanı otomatik olarak geçerli tarih ve saat ile güncelleştirilir.

### <a name="configure-data-validation-project-page"></a>Veri doğrulama projesi sayfasını yapılandır

**Veri doğrulama yapılacaklar işler** çalışma alanını kullanabilmeden önce, işlemi **Veri doğrulama projesini yapılandır** sayfasını kullanarak yapılandırmanız gerekir. (**Çalışma alanları** \> **Veri doğrulama yapılacak işler** \> **Veri doğrulama projesini yapılandır** üzerine tıklayın.)

### <a name="task-areas"></a>Görev alanları

Veri doğrulama görevlerini organizasyonunuz içindeki mantıklı mülkiyet alanlarına gruplandırmak için görev alanlarını kullanırsınız. Örneğin, görev alanları olarak Borç hesapları, Alacak hesapları ve Genel muhasebe kullanılabilir.

**Menü öğesi adı** görev eforuyla ilişkilidir ve çalışma alanındaki görev bağlantısından, ilişkili sayfaya doğrudan gitmek için kullanılabilir. Örneğin, **Borç hesapları yaşlandırma** raporunu, Borç hesapları için çalıştırmak için veri doğrulama görevi, **Borç hesapları yaşlandırma raporu** sayfası üzerinden bağlanabilir.

