---
title: Müşteri için hesaptan ödeme talimatı oluşturma
description: Bu görev kılavuzunda hesaptan ödeme talimatının nasıl oluşturulacağı ve faturada nasıl kullanılacağı gösterilmektedir.
author: ShivamPandey-msft
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0877d437f86f7702aff4019db2c9263a3d8ca4c1
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714271"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Müşteri için hesaptan ödeme talimatı oluşturma

[!include [banner](../../includes/banner.md)]

Bu görev kılavuzunda hesaptan ödeme talimatının nasıl oluşturulacağı ve faturada nasıl kullanılacağı gösterilmektedir.


## <a name="create-a-bank-account"></a>Banka hesabı oluşturun
1. **Gezinti bölmesinde** **Modüller > Alacak hesapları > Müşteriler > Tüm müşteriler**'e gidin.
2. Listeden bir kayıt seçin. Örneğin, TR-001 seçin.
3. Eylem Bölmesinde **Müşteri**'ye tıklayın.
4. **Banka hesapları**'na tıklayın.
5. **Yeni**'ye tıklayın.
6. **Banka hesabı** alanına bir değer girin.
7. **Ad** alanına bir değer yazın.
8. **IBAN** alanına bir değer girin.
9. **Para birimi** alanına bir değer yazın.
10. **Kaydet**'e tıklayın.
11. Sayfayı kapatın.
12. **Gezinti bölmesinde** **Modüller > Nakit ve banka yönetimi > Banka hesapları > Banka hesapları**'na gidin.
13. Listede, istenen kaydı bulun ve seçin.
14. Listede, seçili satırdaki bağlantıya tıklayın.
15. **Düzenle**'yi tıklatın.
16. **Ek kimlik** hızlı sekmesini genişletin.
17. **Otomatik ödeme kodu** alanına bir değer girin.
18. **IBAN** alanına bir değer girin.
19. Sayfayı kapatın.
20. Sayfayı kapatın.

## <a name="define-the-electronic-payment-method"></a>Elektronik ödeme yöntemini tanımlayın
1. **Gezinti bölmesinde** **Modüller > Alacak hesapları > Ödeme ayarı > Ödeme yöntemleri**'ne gidin.
2. **Yeni**'ye tıklayın.
3. **Ödeme yöntemi** alanına bir değer girin.
4. **Tanım** alanına bir değer girin.
5. **Ödeme türü** alanına 'Elektronik ödeme' girin. Ödemenin hesaptan ödeme talimatı yönteminin ödeme türü Elektronik ödeme olmalıdır.
6. **Talimat iste** alanında Evet'i seçin.
7. Sayfayı kapatın.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Müşteriye bir hesaptan ödeme talimatı ekleyin.
1. **Gezinti bölmesinde** **Modüller > Alacak hesapları > Müşteriler > Tüm müşteriler**'e gidin.
2. Listeden bir kayıt seçin. Örneğin, TR-001 seçin.
3. **Düzenle**'yi tıklatın.
4. **Ödeme varsayılanları** hızlı sekmesini genişletin.
5. **Ödeme yöntemi** alanında bir değer girin veya bir değer seçin.
6. **Ödeme varsayılanları** hızlı sekmesini genişletin.
7. **Hesaptan ödeme talimatları** hızlı sekmesini genişletin.
8. **Ekle** öğesine tıklayın.
9. **Banka hesabı** alanında bir değer girin veya seçin.
10. **Alacaklı banka hesabı** alanına bir değer girin veya seçin.
11. **Ödeme sıklığı** alanına bu talimat için işleneceğini tahmin ettiğiniz ödeme sayısını girin.
12. **Tamam**'a tıklayın.
13. **Yazdır**'ı tıklatın.
14. **Talimat raporu**'na tıklayın.
15. Sayfayı kapatın.
16. **Düzenle**'yi tıklatın.
17. **İmza tarihi** alanına bir tarih girin.
18. **Evet** seçeneğini tıklatın.
19. Talimatın imzalandığı yeri girin.
20. **Tamam**'a tıklayın.
21. Sayfayı kapatın.

## <a name="create-a-free-text-invoice-with-mandate"></a>Talimatlı bir serbest metin faturası oluşturun
1. **Gezinti bölmesinde** **Modüller > Alacak hesapları > Faturalar > Tüm serbest metin faturaları**'na gidin.
2. **Yeni**'ye tıklayın.
3. Talimatı eklediğiniz müşteriyi seçin.
4. **Hesaptan ödeme talimatı kodu** alanında bir değer girin veya bir değer seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
