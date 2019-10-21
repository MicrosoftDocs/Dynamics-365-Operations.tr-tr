---
title: Microsoft Project istemci tümleştirmesi
description: Bir proje planı hazırlamak ve sürdürmek karmaşık olabilir bu nedenle proje yöneticilerinin kendilerine görevi yönetmede yardımcı olacak araçlar kullanması gerekir. Microsoft Project İstemcisi ile tümleştirme, bir proje iş kırılım yapısını açmayı ve yönetmeyi destekler.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 610990612d5fb38025bf39cc648d0c9572da37b6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175062"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project istemci tümleştirmesi

[!include [banner](../includes/banner.md)]

Bir proje planı hazırlamak ve sürdürmek karmaşık olabilir bu nedenle proje yöneticilerinin kendilerine görevi yönetmede yardımcı olacak araçlar kullanması gerekir. Microsoft Project İstemcisi ile tümleştirme, bir proje iş kırılım yapısını açmayı ve yönetmeyi destekler. Proje yöneticisi, yaptığı değişiklikleri Dynamics 365 Finance proje iş kırılım yapısına geri yayımlayabilir.

> [!NOTE]
> Temmuz güncelleştirmesini (sürüm 10.0.4) kullanıyorsanız KB 4054797 ve 4055884'ü yüklemeniz gerekir.

## <a name="configure-the-microsoft-project-client-add-in"></a>Microsoft Project İstemcisi eklentisini yapılandırma
Microsoft Project İstemcisiyle tümleştirmeyi etkinleştirmek için, kullanıcının istemcisindeki Microsoft Project uygulamasına bir Microsoft Dynamics 365 eklentisi yüklenmesi gerekir. Bu işlem **Proje yönetimi çalışma alanı** açılarak yapılır.

•   Çalışma alanının **Bağlantılar** > **Kurulum** bölümünden **Proje istemcisi eklentisini yapılandır**'a tıklayın.

•   **Aç**'a ve ardından istendiğinde **Çalıştır**'a tıklayın.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Microsoft Project İstemcisinde mevcut bir taslak iş kırılım yapısını açın ve düzenleyin.
Dynamics 365 Finance'teki bir projede zaten oluşturulmuş bir işi kırılım yapısı varsa, iş kırılım yapısının taslak durumunda olması durumunda iş kırılım yapısı, Microsoft Project Client uygulamasında açılabilir. **Proje** sayfasından açmak için, **Plan** sekmesindeki **Microsoft Project'te aç** bağlantısına tıklayın. Bu sayfa, Microsoft Project İstemcisi uygulaması içinden **Microsoft Dynamics 365** sekmesindeki **Aç** öğesine tıklayarak da açılabilir. **Tüzel kişiliği** ve listeden **Proje**'yi seçin.

> [!NOTE]
> Tarayıcı olarak Internet Explorer kullanıyorsanız, dosyanın indirildiği konumdan el ile açmak için **Kaydet**'e tıklamanız gerekir. Veya, **Kaydet ve aç**'a tıklayarak dosyayı Microsoft Project İstemcisinde açabilirsiniz. Kaydederken dosyayı yeniden adlandırmayın.

Dosyada Microsoft Project Client kullanarak düzenleme yapmadan önce dosyayı kullanıma almanız gerekir. **Microsoft Dynamics 365** sekmesinde **Kullanıma al**'a tıklayın. Böylece, diğer kullanıcıların sizinle aynı anda Finance'ten iş kırılım yapısında düzenleme yapması engellenir. Tüm düzenlemeleri tamamladıktan sonra iş kırılım yapısını yayımlamak için **Microsoft Dynamics 365** sekmesinde **İade et**'e tıklayın.

Bir proje ekibi zaten Finance'teki projeye eklenmişse kaynak listesi, bu ekibin üyeleri ile doldurulur. Projeye henüz atanmış bir proje ekibi yoksa, kaynakları seçebilir ve ekibi Microsoft Project İstemcisi içinde **Microsoft Dynamics 365** sekmesinde yer alan **Kaynaklar**'a tıklayarak oluşturabilirsiniz. 

Aşağıdaki veriler, iade etme işleminin bir parçası olarak Finance ile eşitlenir:

•   Görev adı

•   Başlangıç tarihi

•   Bitiş tarihi

•   Önceller

•   Kaynak adları

•   Kategori

•   Kaynak kategorisi

•   Çalışma saatleri

•   Notlar

•   Öncelik

> [!NOTE]
> Microsoft Project İstemcisi dosyasına başka sütunlar eklerseniz, eklediğiniz sütunlar dosyaya kaydedilmez ve dosya tekrar açıldığında görüntülenmez.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Project İstemcisi'ni kullanarak varolan bir proje için iş kırılım yapısı oluşturma
Microsoft Project İstemcisi'ni kullanarak yeni iş kırılım yapısı oluşturmak için aşağıdaki adımları izleyin:


1.  Microsoft Project İstemcisini açın.

2.  **Microsoft Dynamics 365** sekmesinde **Açık** seçeneğini tıklatın.

3.  Proje için **tüzel kişilik** seçin.

4.  **Proje**'yi seçin.

5.  **Microsoft Dynamics 365** sekmesinde **Kullanıma al**'a tıklayın.

6.  Finance'e yayımlamaya hazır olduğunuzda **Microsoft Dynamics 365** sekmesinde **İade et**'e tıklayın.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Project İstemcisi'ni kullanarak varolan bir proje için mevcut iş kırılım yapısını değiştirme
Microsoft Project İstemcisi kullanarak yeni bir iş kırılım yapısı oluşturmak ve mevcut bir proje için mevcut iş kırılım yapısını değiştirmek için aşağıdaki adımları izleyin:

1.  Microsoft Project İstemcisini açın.

2.  Microsoft Project İstemcisinde planı oluşturun.

3.  **Microsoft Dynamics 365** sekmesinde, **Değişiklikleri kaydet** > **Mevcut projeyi değiştir**'e tıklayın.

4.  Proje için **tüzel kişilik** seçin.

5.  **Proje**'yi seçin.

6.  **Tamam** seçeneğini tıklatın.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Microsoft Project İstemcisinden yeni bir proje oluşturma


1.  Microsoft Project İstemcisini açın.

2.  Microsoft Project İstemcisinde planı oluşturun.

3.  **Microsoft Dynamics 365** sekmesinde, **Değişiklikleri kaydet** > **Yeni Projeye kaydet**'e tıklayın.

4.  Proje için **tüzel kişilik** seçin.

5.  Gerekirse **Proje kodu** girin.

6.  **Proje adı** girin.

7.  **Proje türü**'nü, **Proje grubu**'nu ve **Proje sözleşme kodu**'nu seçin. Alternatif olarak, **Yeni**'ye tıklayarak yeni bir proje sözleşmesi oluşturabilirsiniz.

8.  Kaynak atama için kullanılacak **Takvim**'i seçin.

11. **Tamam** seçeneğini tıklatın.
