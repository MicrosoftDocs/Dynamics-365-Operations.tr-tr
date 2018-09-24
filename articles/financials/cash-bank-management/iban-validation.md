---
title: "Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme"
description: "Bu konuda, Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme işlemi açıklanmaktadır."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: tr-tr
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme

[!include [banner](../includes/banner.md)]

Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulaması bir banka hesabına IBAN eklediğinizde gerçekleştirilen doğrulamanın miktarını artırır.

IBAN'ın yapısı Microsoft Dynamics 365 for Finance and Operation içinde depolanır ve IBAN'ı banka hesaplarında ilk kez kullandığınızda otomatik olarak yüklenir. Banka hesap numarası bir IBAN numarası için tanımlanan yapının parçasıdır. Bu yapıya göre IBAN'daki hesap numarasının konumu ve uzunluğu her ülke veya bölge için yapıda tanımlanan konumla eşleşmezse bir uyarı iletisi alırsınız.

## <a name="set-up-iban-structures"></a>IBAN yapılarını ayarlama

1. **Nakit ve banka yönetimi \> Kurulum \> IBAN yapıları** seçeneğine gidin.
2. Her ülkenin veya bölgenin IBAN yapılarının otomatik olarak ayarlandığına dikkat edin.
3. Yapıları belirli bir ülke veya bölge için özelleştirmeniz gerekirse bunları düzenleyebilirsiniz.
4. Yapı tanımları her yeni sürümün parçası olarak sunulur. **Yapıları sıfırla** menüsünü her güncelleştirmeden sonra en son tanımları yüklemek için kullanabilirsiniz.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Banka hesabındaki IBAN yapısını doğrulama

1. **Nakit ve banka yönetimi \> Banka hesapları \> Banka hesapları** öğesine gidin.
2. Banka hesabı oluşturun.
3. **Ek bilgiler** hızlı sekmesinde bir IBAN girin.

    IBAN'daki hesap numarasının konumu ve uzunluğu her ülke veya bölge için yapıda tanımlanan konumla eşleşmezse bir ileti alırsınız. IBAN'ın uzunluğu IBAN yapısındaki uzunlukla eşleşmezse işleme devam edemezsiniz.

    Doğrulama, banka hesap numarasının IBAN'ın banka hesap numarasını temsil eden kısmıyla eşleştiğini de doğrular. Banka hesap numarası eşleşmiyorsa bir uyarı iletisi alırsınız. Bir ileti yalnızca bir uyarıdır. Banka hesap numarası eşleşmese de işleme devam edebilirsiniz.

