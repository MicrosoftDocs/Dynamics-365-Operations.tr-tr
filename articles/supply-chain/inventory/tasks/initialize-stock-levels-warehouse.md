---
title: "Ambardaki stok düzeylerini başlatma"
description: "Bu yordam, eldeki stoğu, stok hareket günlüğü kullanarak el ile nasıl güncelleştirileceğini gösterir."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 45c93febbbc4ea78fe2b87735ed96fd773605d96
ms.contentlocale: tr-tr
ms.lasthandoff: 09/12/2017

---
# Ambardaki stok düzeylerini başlatma

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

