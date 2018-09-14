--- 
title: "Gelişmiş ambar işlemleri etkinleştirilmiş madde için madde varış günlüğü kullanarak maddeleri kaydetme"
description: "Bu yordam, gelişmiş ambar yönetimi işlemlerini kullanırken ürünlerin ürün varış günlüğü kullanılarak nasıl kaydedileceğini gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 050d1fcbc59d9bb3253bfed2433987285423b334
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Gelişmiş ambar işlemleri etkinleştirilmiş madde için madde varış günlüğü kullanarak maddeleri kaydetme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, gelişmiş ambar yönetimi işlemlerini kullanırken ürünlerin ürün varış günlüğü kullanılarak nasıl kaydedileceğini gösterir. Bu genellikle bir teslim alma memuru tarafından yapılır. 

Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde çalıştırabilirsiniz. Bu kılavuzu başlatmadan önce, elinizde açık bir satınalma sipariş satırı içeren onaylı bir satınalma siparişi bulunması gerekir. Satırdaki madde stokta olmalı, ürün çeşitleri kullanmamalı ve izleme boyutları olmamalıdır. Ayrıca, ürünün ambar yönetimi işlemi etkin bir depolama boyut grubuyla ilişkilendirilmesi gerekir. Kullanılan ambar, ambar yönetimi işlemleri için etkinleştirilmelidir ve alım işlemi için kullanılan yerleşimin plakası kontrol edilmiş olmalıdır. USMF kullanıyorsanız, SAS oluşturmak için şirket hesabı 1001, ambar 51 ve ürün M9200 değerlerini kullanabilirsiniz. 

Oluşturduğunuz satınalma siparişinin numarasınının yanı sıra, satınalma siparişi satırı için kullandığınız ürün numarası ve tesisi de not edin .


## <a name="create-an-item-arrival-journal-header"></a>Bir ürün varış günlüğü başlığı oluşturma
1. Ürün varışı'na gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
    * USMF kullanıyorsanız, WHS yazabilirsiniz. Başka veriler kullanıyorsanız, adını seçtiğiniz günlükte iki özelliğin olması gerekir: Malzeme çekme yerleşimini denetle ayarı Hayır, Karantina yönetimi ayarı Hayır olmalıdır.  
4. Numara alanına bir değer girin.
5. Tesis alanına bir değer yazın.
    * Satınalma siparişi satırı için kullanılacak tesisi seçin. Bu, günlükteki tüm satırlar için varsayılan olan bir varsayılan değer işlevi görür. USMF'de ambar 51'i kullandıysanız, tesis 5'i seçin.  
6. Ambar alanına bir değer yazın.
    * Seçmiş olduğunuz tesis için geçerli bir ambar seçin. Bu, günlükteki tüm satırlar için varsayılan olan bir varsayılan değer işlevi görür. USMF'te örnek değerler kullanıyorsanız, 51'i seçin.  
7. Yerleşim alanına bir değer girin.
    * Seçmiş olduğunuz ambar için geçerli bir yerleşim seçin. Yerleşim, plakanın kontrol edildiği bir yerleşim profiliyle ilişkili olmalıdır. Bu, günlükteki tüm satırlar için varsayılan olan bir varsayılan değer işlevi görür. USMF'te örnek değerler kullanıyorsanız, Bulk-008'i seçin.  
8. Plaka alanında aşağı açılan oku sağ tıklatın ve sonra Ayrıntıları göster'i seçin.
9. Yeni'ye tıklayın.
10. Plaka alanında bir değer girin.
    * Değerini not edin.  
11. Kaydet'e tıklayın.
12. Sayfayı kapatın.
13. Plaka alanında bir değer girin.
    * Yeni oluşturduğunuz plakanın değerini girin. Bu, günlükteki tüm satırlar için varsayılan olan bir varsayılan değer işlevi görür.  
14. Tamam'a tıklayın.

## <a name="add-a-line"></a>Bir satır ekleyin
1. Satır ekle'ye tıklayın.
2. Madde numarası alanına bir değer girin.
    * Satınalma siparişi satırında kullandığınız ürün numarasını girin.  
3. Miktar alanına bir sayı girin.
    * Kaydetmek istediğiniz miktarı girin.  
    * Tarih alanı, bu ürünün eldeki miktarın stokta kaydedileceği tarihi belirler.  
    * Lot kodu sağlanan bilgilerden hareketle benzersiz şekilde tanımlanabiliyorsa, sistem tarafından doldurulur. Aksi halde, bunu el ile eklemeniz gerekir. Bu, bu kaydı belirli bir kaynak belge satırına bağlayan zorunlu bir alandır.  

## <a name="complete-the-registration"></a>Kaydı tamamlama
1. Doğrula'ya tıklayın.
    * Bu günlüğün deftere nakile hazır olup olmadığını denetler. Doğrulama başarısız olursa, günlüğü deftere nakledebilmek için hataları düzeltmeniz gerekir.  
2. Tamam'a tıklayın.
    * Tamam düğmesini tıklattıktan sonra iletiyi gözden geçirin. Günlükte sorun olmadığını belirten bir ileti görünmesi gerekir.  
3. Deftere Naklet öğesine tıklayın.
4. Tamam'a tıklayın.
    * Tamam düğmesine tıkladıktan sonra ileti çubuğunu kontrol edin. İşlemin tamamlandığını belirten bir ileti görünmesi gerekir.  
5. Sayfayı kapatın.


