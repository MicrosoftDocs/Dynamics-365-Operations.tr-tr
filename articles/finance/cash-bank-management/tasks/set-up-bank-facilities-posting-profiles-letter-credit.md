---
title: Kredi mektubu için banka hizmetlerini ve banka deftere nakil profillerini ayarlama
description: Bu yordam, akreditif mektubunu işlemek için gerekli olan banka tesisi ve nakletme profilini oluşturmayı gösterir.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fe5b2ba43c4fcb4855c742bdb6f8209ebd92d68
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779475"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Kredi mektubu için banka hizmetlerini ve banka deftere nakil profillerini ayarlama

[!include [banner](../../includes/banner.md)]

Bu yordam, akreditif mektubunu işlemek için gerekli olan banka tesisi ve nakletme profilini oluşturmayı gösterir. 

Bu görevler, USMF demo şirketini kullanır.


## <a name="general-ledger-parameter"></a>Genel muhasebe defteri parametresi
1. **Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri**'ne gidin.
2. **Banka belgesi** bölümünü genişletin.
3. **Kredi mektubunu içe aktarmayı etkinleştir**'i seçin.
4. **Kredi mektubunu dışarı aktarı etkinleştir**'i seçin.
5. **Kaydet**'e tıklayın.
6. Sayfayı kapatın.

## <a name="create-bank-facility"></a>Banka hizmeti yarat
1. **Nakit ve Banka yönetimi > Kurulum > Banka tesisleri** seçeneğine gidin.
2. **Yeni**'yi tıklatın.
3. **Tesis grubu** alanında, banka tesisi grup adını girin.
4. **Açıklama** alanında, banka tesisi grup tanımını girin.
5. **Kaydet**'e tıklayın.
6. **Tesis türleri** sekmesine tıklayın.
7. **Yeni**'yi tıklatın.
8. **Tesis türü** alanına benzersiz bir kod yazın.
9. **Tanım** alanına bir değer girin.
10. **Tesis grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
11. Listede, istenen kaydı bulun ve seçin.
12. Listede, seçili satırdaki bağlantıya tıklayın.
13. **Tesis niteliği** alanında banka tesisinin niteliğini seçin.
14. **Kaydet**'e tıklayın.
15. Sayfayı kapatın.

## <a name="bank-posting-profile"></a>Banka nakil profili
1. **Nakit ve Banka yönetimi > Kurulum > Banka belgesi deftere nakil profili** seçeneğine gidin.
2. **Yeni**'yi tıklatın.
3. **Hesap/Grup numarası** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Hesap kesme için ana hesabı seçin.
    * Nakit akışı tahminini hesaplarken bu hesap kullanılır.  
7. **Gider hesabı** alanında masraf hareketleri hesabını seçin.
8. **Marj hesabı** alanında marj hareketleri hesabını seçin.
    * Bu hesaba açılış marjı nakledilirken alacak, ödeme nakledilirken ise borç kaydedilir.  
9. **Kaydet**'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
