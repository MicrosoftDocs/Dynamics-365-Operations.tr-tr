--- 
title: "Bir satıcı hesabı oluşturma"
description: "Bu yordam, bir satıcı hesabı oluşturmayı ve adres ve kişi bilgileri eklemeyi göstermektedir."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6ff2357d5266c45be2f403e463c72089d73db21b
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-account"></a>Bir satıcı hesabı oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir satıcı hesabı oluşturmayı ve adres ve kişi bilgileri eklemeyi göstermektedir. Bu yordam satınalma ve finansal amaçlar için olan tüm alanları doldurmayı göstermez. Bu alanlar hakkında daha fazla bilgi için lütfen alan açıklamalarını okuyun. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Satıcı hesapları genellikle bir satınalma profesyoneli veya alacak hesapları personeli tarafından oluşturulur.


## <a name="create-a-vendor-account"></a>Bir satıcı hesabı oluşturma
1. Tedarik ve kaynak > Satıcılar > Tüm satıcılar'a tıklayın.
2. Yeni'ye tıklayın.
3. Satıcı hesabı alanına bir değer girin.
    * Değer otomatik olarak girilir. Bu durumda, bu adımı atlayabilirsiniz.  
    * Bir kişi veya kuruluş için satıcı hesapları oluşturabilirsiniz. Bu, hangi alanların kullanılabileceğini etkiler. Bu örnekte, bir organizasyon için bir satıcı hesabı oluşturacağız.   
4. Ad alanına bir değer girin veya buradan bir değer seçin.
    * Satıcı ise bir zaten sisteminizde kayıtlı bir tarafsa, açılan aşağı menüyü kullanarak satıcıyı bu alanda seçerseniz, yeni bir satıcı hesabı zaten kayıtlı adres ve ilgili kişi bilgilerini devralır.  
5. Grup alanına bir değer girin veya buradan bir değer seçin.
    * Satıcı grubu aşağıdaki parametrelerden herhangi birine ortak olarak sahip olan satıcıları gruplandırmak için kullanılır: Ödeme koşulları, kapatma dönemi, satış vergisi grubu da dahil olmak üzere genel muhasebe hesapları, stok defterine nakil grupları; varsayılan genel muhasebe hesapları; ürün kodlarını filtre ve tahmin yapılandırması.  
6. Personel sayısı alanına bir sayı girin.
7. Organizasyon numarası alanında bir değer girin.

## <a name="add-an-address"></a>Bir adres ekleyin
1. Adresler bölümünü genişletin.
2. Ekle öğesini tıklatın.
3. Amaç alanına bir değer girin veya buradan bir değer seçin.
    * Bir veya daha fazla sayıda amaç seçebilirsiniz. Bunlar belirli bir amaç için doğru adresin seçilmesi için kullanılır. Örneğin, amaç “Fatura” ise, faturalar gönderilirken bu adres kullanılır.  
4. Ad veya açıklama alanına bir değer yazın.
5. Ülke/bölge alanına bir değer girin veya buradan bir değer seçin.
    * Adresi ayrıntılarını girin. Seçtiğiniz ülke/bölge, ülke/bölge adres biçimine karşılık gelerek size sunulacak olan alanları belirleyecektir.   
6. Tamam'a tıklayın.

## <a name="add-contact-information"></a>İletişim bilgileri ekleyin
1. Ekle öğesini tıklatın.
2. Açıklama alanına bir değer girin.
3. Tür alanında, bir seçenek seçin.
4. İletişim numarası/adresi alanında bir değer girin.
    * Birincil ilgili kişi ise, Birincil onay kutusunu işaretleyebilirsiniz.  
5. Kaydet'e tıklayın.
6. Sayfayı kapatın.
7. Sayfayı kapatın.


