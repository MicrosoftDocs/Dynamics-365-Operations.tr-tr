---
title: Yeni proje oluştur
description: Bu konuda yeni bir proje oluşturma hakkında bilgiler yer alır.
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
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760683"
---
# <a name="create-a-new-project"></a>Yeni proje oluştur

[!include [banner](../includes/banner.md)]

Yeni bir proje oluşturmak için aşağıdaki adımları tamamlayın.

1. **Proje yönetimi** sayfasında **Yeni proje**'yi seçin ve aşağıdaki değerleri girin:

    - **Proje türü:** Zaman ve malzeme
    - **Proje adı:** XYZ Yükseltme Aşaması 2
    - **Proje grubu:** TM\_WIP
    - **Proje sözleşme kodu:** 00000002

2. **Proje oluştur**'u seçin.

## <a name="assign-a-resource-to-a-project"></a>Projeye kaynak atama

1. **Çalışanlar** sayfasında, **Çalışanlar** listesinde, daha önce yetkinlikleri ayarladığınız çalışanın kaydını seçin ve çalışan kaydını açın.
2. Eylem Bölmesinde, **Proje** sekmesindeki **Ayar** gurubunda **Projeleri ata**'yı seçin.
3. **Kaynak doğrulama proje atamaları** sayfasında, **Projeler** sekmesinde, **Projeyi seçilen projelere ekle** alanında, **XYZ Yükseltme Aşaması 2** projesinde filtreleyin.
4. **Kalan projeler** bölmesinde, bir proje seçin ve ardından **Seçilen projeler** bölmesine eklemek için ok düğmesini seçin.

Gerekirse, kaynak için kategoriler de atayabilirsiniz. Kategori türü **Maliyet** veya **Gelir**'dir. Kategori türü, kuruluşunuz tarafından belirlenir. Kaynak için hiçbir kategori atanmamışsa Finance, maliyet ve gelir için saat fiyatlarında varsayılan kategoriyi arar.

## <a name="set-up-project-resource-and-role-characteristics"></a>Proje kaynağını ve rol özelliklerini ayarlama

Proje yöneticisi, bir proje için gerekli olan rolleri oluşturmak için proje kaynak oluşturma işlevini kullanabilir. Roller, teyit edilen kaynaklar kaynaklar rezerve edildiğinde hala bilinmediğinde kullanılabilir. Roller geçici olarak planlanan kaynak olarak kullanılabilir; bu durumda proje planlama aşamalarına devam edebilirsiniz.

[![Rol örneği](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Senaryo:** Contoso, onaylanmış bir proje tüzüğü olan bir Zaman ve malzeme projesini tamamlamak üzere işe alınmıştır. Yardımcı proje müdürü, projenin amacını doldurmaya devam etmektedir. Kaynak yöneticisi, yeni projede çalışmak üzere rezerve edilecek belirli kaynakları belirlemektedir. Projenin kritik doğası sebebiyle, proje sponsoru, Kıdemli proje yöneticisini rollerden biri olarak talep etmiştir. Kaynak yöneticisinin yeni bir kaynak alması ve yardımcı proje yöneticisi için proje planlama sırasında kaynak bilgisi gerekli olduğundan, rolü sistemde tanımlamalıdır.

Aşağıdaki adımlarda, kaynak yöneticisinin Kıdemli proje yöneticisi rolünü nasıl ayarlayabileceği ve kaynak özelliklerini bununla nasıl ilişkilendirebileceği gösterilmektedir. Daha sonra, rol istenen kaynak yetkinlikleriyle eşleşen kullanılabilir kaynakları aramak için kullanılabilir.

1. **Kurulum rolleri** sayfasında **Yeni**'yi seçin ve aşağıdaki değerleri girin:

    - **Rol Kimliği:** Kıdemli Proje Yöneticisi
    - **Açıklama:** Kıdemli Proje Yöneticisi

2. **Oluştur**'u seçin.
3. **Kıdemli Proje Yöneticisi** rolünü seçip **Özellikleri yapılandır**'ı tıklatın.
4. **Özelliklerin türü** alanında, **Beceri**'yi seçin.
5. **Kullanılabilir özellikler** alanına, aradığınız yeteneği girin.
6. **Özellik türü** alanında **Sertifika**'yı seçin.
7. **Kullanılabilir özellikler** alanına, aradığınız sertifika türünü girin.

## <a name="assign-a-project-resource-to-a-project"></a>Projeye proje kaynağı atama

1. **Tüm projeler** sayfasında, **XYZ Yükseltme Aşaması 2** projesini seçin.
2. **Proje ekibi ve planlama** sekmesinde **Ekle**'yi seçin.
3. **Rol** alanında **Ekip üyesi**'ni seçin.
4. **Takvimden rezerve et**'i seçin.
5. **Kaynak kullanılabilirliği** sayfasında, **Görünüm ayarları**'nı seçin.
6. **Görünüm ayarlarını ayarla** sayfasına şu değerleri girin:

    - **Tarih aralığı görünüm biçimi:** Gün
    - **Uygunluk açıklamalarını görüntüle:** Evet
    - **Kalan kapasiteyi görüntüle:** Evet

7. Kaynak listesinde, bir kaynak seçin.
8. **Sabit defter** ve **Tam kapasite**'yi seçin.

## <a name="assign-a-resource-to-a-default-role"></a>Varsayılan bir role kaynak atama

Proje veya kaynak yöneticilerine yardımcı olmak için, bir proje için rezerve edilebilecek kaynaklarla ilgili daha ayrıntılı inceleme yapabilirsiniz. Varsayılan bir rolü mevcut bir kaynakla veya yeni edinilen bir kaynakla ilişkilendirebilirsiniz. örneğin, Daniel işe alındığında, İş analisti rolünü yerine getirmek için beceri ve deneyimi vardı. Kaynak yöneticisi, bu rolü Daniel'ın varsayılan rolü olarak atadı. Bu nedenle, kaynak yöneticisi Daniel'ı projelerde çalışmak üzere kullanılabilir olan iş analistleri havuzuna eklendi.

Kaynak rezervasyonu sırasında, proje yöneticileri projede çalışabilecek rol kaynaklarını filtreleyebilir. Bu bilgiyi, kaynak karşılama sırasında çok ölçütlü karar analizi gerçekleştirirken bir ölçüt olarak kullanabilirler. Ayrıca, söz konusu proje için belirli becerileri, eğitimi ve deneyimi olan kaynakları aramak için filtre uygulamak amacıyla diğer kaynak özelliklerini ekleyebilirler.

**Senaryo:** Onaylanmış bir proje başlamıştır ve Kıdemli proje yöneticisi rolü proje planlama aşamasında planlanan kaynak olarak rezerve edilmiştir. Kaynak yöneticisi, Kıdemli proje yöneticisi rolünü yerine getirecek bir kaynak edinmiştir.

1. **Kaynaklar listesi** sayfasında, **Daniel Goldschmidt**'i seçin.
2. **Kaynak rolleri** sayfasında **Yeni**'yi seçin ve aşağıdaki değerleri girin:

    - **Yürürlük başlangıcı:** Geçerli tarihi girin.
    - **Bitiş:** **Asla** girin.
    - **Rol:** **Kıdemli Proje Yöneticisi** girin.

3. **Kaydet**'i seçip sayfayı kapatın.
4. **Yetkinlikler** sekmesinde, **ProjectMgmt** becerisini ve **PMP** sertifikasını ekleyin.
