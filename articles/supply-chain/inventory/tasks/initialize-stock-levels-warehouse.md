---
title: Ambardaki stok düzeylerini başlatma
description: Bu yordam, eldeki stoğu, stok hareket günlüğü kullanarak el ile nasıl güncelleştirileceğini gösterir.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6934fc8142a589532cbd9d360ca0f8276456b20e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011567"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Ambardaki stok düzeylerini başlatma

[!include [banner](../../includes/banner.md)]

Bu yordam, eldeki stoğu, stok hareket günlüğü kullanarak el ile nasıl güncelleştirileceğini gösterir. (Ayrıca, eldeki stoğu, veri varlıklarındaki hareketleri içeri alarak güncelleştirmek mümkündür.) Bu kılavuzu içerisinde , günlük adı, Madde Kurulumu, nakil profilleri, ve mevcut hesapların da arasında olduğu tüm önkoşulları bulunduran, demo veri şirketi USMF verilerini kullanarak çalıştırabilirsiniz. Bu rehber kullanılan madde ve boyutlar için belirli değerler önerir. Farklı bir öğeyi seçerseniz, farklı boyutlar için değerler girmeniz gerekebilir.

1. Stok yönetimi > Yevmiye defteri girişleri > Öğeler > Taşıma seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. IMov'u seçin.
    * Farklı günlük adı şablonlarını farklı ticari amaçlarla kullanmak iyi bir uygulamadır.  
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Mahsup hesabı alanında, '140200' değerlerini seçin.
    * Bu mahsup hesap, günlük satırlarındaki varsayılan olarak belirlenecek hesaptır. Her satırda farklı mahsup hesapları atamak için varsayılan geçersiz kılmak mümkündür.  
7. Tamam'a tıklayın.
8. Yeni'ye tıklayın.
9. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
10. Madde A0001'i seçin.
11. Listede, seçili satırdaki bağlantıya tıklayın.
12. Stok boyutları sekmesini tıklatın.
13. Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.
14. Saha 1'i seçin.
15. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
16. Ambar 13'ü seçin.
17. Listede, seçili satırdaki bağlantıya tıklayın.
18. Yerleşim alanında, açılır menü düğmesine tıklayarak aramayı açın.
19. Yer 13'ü seçin.
20. Miktar alanına bir sayı girin.
21. Kaydet'e tıklayın.
22. Deftere Naklet öğesine tıklayın.
23. Tüm deftere nakil hatalarını yeni bir günlüğe aktar onay kutusunun işaretleyin veya işaretini kaldırın.
    * Bu seçeneği etkinleştirirseniz, deftere nakledilmede başarısız olan satırlar yeni bir günlüğe kopyalanacaktır. Sorunları düzeltmek ve satırları daha sonra yeniden deftere nakletmek için günlükteki bilgileri kullanın.  
24. Tamam'a tıklayın.
25. Sayfayı kapatın.
26. Sayfayı kapatın.

