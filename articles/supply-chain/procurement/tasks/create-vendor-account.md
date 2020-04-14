---
title: Bir satıcı hesabı oluşturma
description: Bu yordam, bir satıcı hesabı oluşturmayı ve adres ve kişi bilgileri eklemeyi göstermektedir.
author: mkirknel
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba585a9bb1a296bbf7181530e151d737bfa22fc2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149608"
---
# <a name="create-a-vendor-account"></a>Bir satıcı hesabı oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, bir satıcı hesabı oluşturmayı ve adres ve kişi bilgileri eklemeyi göstermektedir. Bu yordam satınalma ve finansal amaçlar için olan tüm alanları doldurmayı göstermez. Bu alanlar hakkında daha fazla bilgi için lütfen alan açıklamalarını okuyun. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Satıcı hesapları genellikle bir satınalma profesyoneli veya alacak hesapları personeli tarafından oluşturulur.


## <a name="create-a-vendor-account"></a>Satıcı hesabı oluşturma
1. **Gezinti Bölmesi > Modüller > Tedarik ve kaynak atama > Satıcılar > Tüm satıcılar**'a gidin.
2. **Yeni**'ye tıklayın.
3. **Satıcı hesabı** alanına bir değer girin.
    - Değer otomatik olarak girilir. Bu durumda, bu adımı atlayabilirsiniz.  
    - Bir kişi veya kuruluş için satıcı hesapları oluşturabilirsiniz. Bu, hangi alanların kullanılabileceğini etkiler. Bu örnekte, bir organizasyon için bir satıcı hesabı oluşturacağız.   
4. **Ad** alanına bir değer girin veya buradan bir değer seçin. Satıcı ise bir zaten sisteminizde kayıtlı bir tarafsa, açılan aşağı menüyü kullanarak satıcıyı bu alanda seçerseniz, yeni bir satıcı hesabı zaten kayıtlı adres ve ilgili kişi bilgilerini devralır.
5. **Grup** alanına bir değer girin veya buradan bir değer seçin. Satıcı grubu aşağıdaki parametrelerden herhangi birine ortak olarak sahip olan satıcıları gruplandırmak için kullanılır: Ödeme koşulları, kapatma dönemi, satış vergisi grubu da dahil olmak üzere genel muhasebe hesapları, stok defterine nakil grupları; varsayılan genel muhasebe hesapları; ürün kodlarını filtre ve tahmin yapılandırması.
6. **Personel sayısı** alanına bir sayı girin.
7. **Kuruluş numarası** alanında bir değer girin.

## <a name="add-an-address"></a>Bir adres ekleyin
1. **Adresler** bölümünü genişletin.
2. **Ekle** öğesine tıklayın.
3. **Amaç** alanına bir değer girin veya buradan bir değer seçin. Bir veya daha fazla sayıda amaç seçebilirsiniz. Bunlar belirli bir amaç için doğru adresin seçilmesi için kullanılır. Örneğin, amaç “Fatura” ise, faturalar gönderilirken bu adres kullanılır.
4. **Ad veya açıklama** alanına bir değer yazın.
5. **Ülke/bölge** alanına bir değer girin veya buradan bir değer seçin. Adresi ayrıntılarını girin. Seçtiğiniz ülke/bölge, ülke/bölge adres biçimine karşılık gelerek size sunulacak olan alanları belirleyecektir. 
6. **Tamam**'a tıklayın.

## <a name="add-contact-information"></a>İletişim bilgileri ekleyin
1. **İletişim bilgileri** bölümünü genişletin veya daraltın.
2. **Ekle** öğesine tıklayın.
3. **Tanım** alanına bir değer girin.
4. **Tür** alanında, bir seçenek belirtin.
5. **İletişim numarası/adresi** alanında bir değer girin. Birincil ilgili kişi ise, Birincil onay kutusunu işaretleyebilirsiniz.  
6. **Kaydet**'e tıklayın.
7. Sayfayı kapatın.
8. Sayfayı kapatın.

