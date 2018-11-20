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
ms.sourcegitcommit: c6502a6fb0ceaed75fd5bb6ec5b2f13db1879eea
ms.openlocfilehash: 19e0528b95952de8e5503c361efcfeca4c529caf
ms.contentlocale: tr-tr
ms.lasthandoff: 10/12/2018

---

# <a name="manage-international-bank-account-number-iban-validation"></a>Uluslararası Banka Hesap Numarası (IBAN) doğrulamasını yönetme

[!include [banner](../includes/banner.md)]

Uluslararası Banka Hesap Numarası (IBAN) doğrulaması bir banka hesabına IBAN eklediğinizde gerçekleştirilen doğrulamanın miktarını artırır.

IBAN'ın yapısı hakkında bilgiler Microsoft Dynamics 365 for Finance and Operations içinde depolanır. Banka hesaplarında IBAN'ı ilk kez kullandığınızda, bu bilgiler otomatik olarak yüklenir. IBAN uzunluğu, banka hesap numarasının başlangıç konun ve rota numarası, banka hesap numarası uzunluğu ve rota numarasını içerir.

## <a name="set-up-iban-structures"></a>IBAN yapılarını ayarlama

1. **Nakit ve banka yönetimi \> Kurulum \> IBAN yapıları** seçeneğine gidin.
2. Her ülkenin veya bölgenin IBAN yapılarının otomatik olarak ayarlandığına dikkat edin.
3. Yapıları belirli bir ülke veya bölge için özelleştirmek isterseniz bunları düzenleyebilirsiniz.
4. Yapı tanımları her yeni sürümün parçası olarak sunulur. **Yapıları sıfırla** menüsünü her güncelleştirmeden sonra en son tanımları yüklemek için kullanabilirsiniz.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Banka hesabındaki IBAN yapısını doğrulama

1. **Nakit ve banka yönetimi \> Banka hesapları \> Banka hesapları** öğesine gidin.
2. Banka hesabı oluşturun.
3. **Ek bilgiler** hızlı sekmesinde bir IBAN girin.

    Her ülke veya bölge için tanımlanan uzunlukla IBAN'ın uzunluğu eşleşmiyorsa, bir uyarı iletisi alacaksınız. IBAN'ın uzunluğu IBAN yapısında belirtilen uzunlukla eşleşmezse işleme devam edemezsiniz.

    Doğrulama, banka hesap numarasının IBAN'ın banka hesap numarasını temsil eden kısmıyla eşleştiğini de doğrular. Banka hesap numarası eşleşmiyorsa bir uyarı iletisi alırsınız. Bir ileti yalnızca bir uyarıdır. Banka hesap numarası eşleşmese de işleme devam edebilirsiniz.

    Doğrulama, banka rota numarasının IBAN'ın banka rota numarasını temsil eden kısmıyla eşleştiğini de doğrular. Rota numarası, banka numarası ve genellikle bir ek banka şubesi içerir. Banka rota numarası eşleşmiyorsa bir uyarı iletisi alırsınız. Bir ileti yalnızca bir uyarıdır. Banka rota numarası eşleşmese de işleme devam edebilirsiniz.

