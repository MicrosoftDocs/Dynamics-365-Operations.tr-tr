---
title: Teminat mektupları için banka hizmetlerini ve banka deftere nakil profillerini ayarlama
description: Bu görev, garanti mektubu işlemek için gereken banka tesisi ve deftere nakil profilini oluşturur.
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
ms.openlocfilehash: 0987ae1e9cfbb1e2d2a957a5fd1ad82257292c0a
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804114"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Teminat mektupları için banka hizmetlerini ve banka deftere nakil profillerini ayarlama

[!include [banner](../../includes/banner.md)]

Bu görev, garanti mektubu işlemek için gereken banka tesisi ve deftere nakil profilini oluşturur.



Bu görevde USMF demo şirketi kullanılmaktadır. 




## <a name="general-ledger-parameter"></a>Genel muhasebe defteri parametresi
1. **Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri**'ne gidin.
2. **Banka belgesi** bölümünü genişletin.
3. **Teminat mektubunu etkinleştir** seçeneğini seçin.
4. **Hareket günlüğü** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, istenen kaydı bulun ve seçin.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. **Numara sıraları** sekmesine tıklayın.
    * Teminat mektubu numarası ve teminat mektubu hareket referansı için sayı sıra numarası kodunu tanımlayın.  
8. **Kaydet**'e tıklayın.
9. Sayfayı kapatın.

## <a name="create-bank-facility"></a>Banka hizmeti yarat
1. **Nakit ve Banka yönetimi > Kurulum > Banka tesisleri** seçeneğine gidin.
2. **Yeni**'yi tıklatın.
3. **Tesis grubu** alanına, teminat mektubu hareketi için banka tesisi grup adını girin.
4. **Tanım** alanına bir değer girin.
5. **Kaydet**'e tıklayın.
6. **Tesis türleri** sekmesine tıklayın.
7. **Yeni**'yi tıklatın.
8. **Tesis türü** alanında, banka tesisi anlaşmasıyla ilişkili banka tesisi türünün adını girin.
9. **Tanım** alanına bir değer girin.
10. **Tesis grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
11. Listede, istenen kaydı bulun ve seçin.
12. Listede, seçili satırdaki bağlantıya tıklayın.
13. **Tesis niteliği** alanında, bir seçenek seçin.
14. **Kaydet**'e tıklayın.
15. Sayfayı kapatın.

## <a name="bank-posting-profile"></a>Banka nakil profili
1. **Nakit ve Banka yönetimi > Kurulum > Banka belgesi deftere nakil profili** seçeneğine gidin.
2. **Yeni**'yi tıklatın.
3. **Hesap/Grup numarası** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. **Kapatma hesabı** alanında, hesap kapatma için ana hesabı seçin.
7. **Gider hesabı** alanında masraf hareketleri hesabını seçin.
8. **Marj hesabı** alanında, marj hareketi hesabını seçin.
9. **Tasfiye hesabı** alanında, teminat mektubu hareketi için tasfiye hesabını seçin. 
10. **Kaydet**'e tıklayın.
11. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
