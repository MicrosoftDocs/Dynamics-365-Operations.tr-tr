---
title: Satış vergisi ödemeleri ve yuvarlama kuralları
description: Bu konuda, Satış vergisi makamlarında yuvarlama kuralı ayarlarının nasıl çalıştığı ve Satış vergilerini kapatma ve deftere nakletme işi sırasında satış vergisi bilançosunun yuvarlanması açıklanmaktadır.
author: kailiang
ms.date: 10/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a75d41195875c5ed48cbe8ce5f5e448f173e718
ms.sourcegitcommit: 4f8465729d7ae0bf5150a2785a6140c984c7030e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2021
ms.locfileid: "7726812"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Satış vergisi ödemeleri ve yuvarlama kuralları

[!include [banner](../includes/banner.md)]

Bu konuda, Satış vergisi makamlarında yuvarlama kuralı ayarlarının nasıl çalıştığı ve Satış vergilerini kapatma ve deftere nakletme işi sırasında satış vergisi bilançosunun yuvarlanması açıklanmaktadır.

Satış vergilerinin düzenli olarak vergi dairelerine bildirilmesi ve ödenmesi gerekir. Bu eylem, **Satış vergisi** sayfasındaki Satış vergisi kapatma ve nakletme işlemi çalıştırılarak yapılabilir. Bir döneme ait satış vergisi, satış vergisi hesaplarına karşı kapatılır ve satış vergisi bakiyesi Satış vergisi kapatma hesabına nakledilir. Satış vergisi kapatma hesabına nakledilen satış vergisi bakiyesi, **Satş vergisi** sayfasında bir yuvarlama kuralı ayarlanarak vergi kurumlarının gerektirdiği şekilde yuvarlanabilir. 

Yuvarlama farkı, Genel muhasebenin Otomatik hareketler için hesaplar alanında seçilen Satış vergisi yuvarlama hesabına nakledilir.

Aşağıdaki örnekte, Satış vergisi dairesinde yuvarlama kuralının nasıl işlediği gösterilmektedir.

## <a name="examples"></a>Örnekler

Bir döneme ilişkin toplam satış vergisi alacak bakiyesi -98.765,43 olarak görünmektedir. Tüzel kişilik ödediğinden daha fazla satış vergisi tahsil etmiştir. Bu nedenle, tüzel kişiliğin vergi dairesine ödeme yapması gerekir. 

Tüzel kişilik bakiyeyi en yakın 1,00 değerine yuvarlayan bir yuvarlama yöntemi kullanmak istemektedir. Satış vergisi muhasebesinden sorumlu kullanıcı aşağıdaki adımlardan birini gerçekleştirmelidir:

1. **Vergi** >  **Dolaylı vergiler** > **Satış vergisi** > **Satış vergisi dairesi** öğelerine tıklayın.
2. **Genel** hızlı sekmesinde, **Yuvarlama formu** alanından **Normal** seçeneğini seçin.
3. **Yuvarlama** alanına 1,00 girin.
4. Satış vergisini vergi dairesine ödeme zamanı geldiğinde, **Veri** > **Beyannameler** > **Satış vergisi** > **Satış vergisini kapat ve deftere naklet**'e gidin. Satış vergisi kapatma hesabındaki **98.765,43** tutarındaki vergi borcunun **98.765**'e yuvarlandığını görebilirsiniz.

Aşağıdaki tabloda, 98.765,43 tutarının **Satış vergisi dairesi** sayfasındaki **Yuvarlama formu** alanında bulunan her yuvarlama yöntemi kullanılarak nasıl yuvarlandığı gösterilmektedir.

> [!NOTE]                                                                                  
> Yuvarlama değeri 0,00 olarak ayarlanmışsa,:
>
> - Normal yuvarlama için, yuvarlama davranışı **Yuvarla = 0,01** ile aynıdır.
> - **Yuvarlama formu seçenekleri** **Aşağı doğru**, **Yukarı yuvarlama** ve **Kendi avantajı** için, davranış **Yuvarla = 1,00** ile aynıdır.

| Yuvarlama formu seçeneği                | Yuvarlama değeri = 0,01 | Yuvarlama değeri = 0,10 | Yuvarlama değeri = 1,00 | Yuvarlama değeri = 100,00 | Yuvarlama değeri = 0,00   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| Normal                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                | 98,765.43                |
| Aşağı yuvarlama                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Yukarı yuvarlama                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |
| Kendi avantajı, alacak bakiyesi için | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Kendi avantajı, borç bakiyesi için  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |

### <a name="normal-round-and-round-precision-is-001"></a>Normal yuvarlama, yuvarlama hassasiyeti 0,01'dir

```<table>
  <tr>
    <td>Rounding
    </td>
    <td>Calculation process
    </td>
  </tr>
    <tr>
    <td>round(1.015, 0.01) = 1.02
    </td>
    <td>
      <ol>
        <li>round(1.015 / 0.01, 0) = round(101.5, 0) = 102
        </li>
        <li>102 * 0.01 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.014, 0.01) = 1.01
    </td>
    <td> <ol>
        <li>round(1.014 / 0.01, 0) = round(101.4, 0) = 101
        </li>
        <li>101 * 0.01 = 1.01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.011, 0.02) = 1.02
    </td>
    <td> <ol>
        <li>round(1.011 / 0.02, 0) = round(50.55, 0) = 51
        </li>
        <li>51 * 0.02 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.009, 0.02) = 1.00
    </td>
    <td> <ol>
        <li>round(1.009 / 0.02, 0) = round(50.45, 0) = 50
        </li>
        <li>50 * 0.02 = 1.00
        </li>
      </ol>
    </td>
  </tr>
</table>
```

> [!NOTE]                                                                                  
> Kendi avantajı seçeneğini seçerseniz, yuvarlama daima tüzel kişiliğin yararına yapılır. 

Daha fazla bilgi için aşağıdaki konulara bakın:
- [Satış vergisine genel bakış](indirect-taxes-overview.md)
- [Satış vergisi ödemesi oluşturma](tasks/create-sales-tax-payment.md)
- [Belgelerde satış vergisi hareketleri oluşturma](tasks/create-sales-tax-transactions-documents.md)
- [Deftere nakledilen satış vergisi hareketlerini görüntüleme](tasks/view-posted-sales-tax-transactions.md)
- [yuvarla işlevi](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
