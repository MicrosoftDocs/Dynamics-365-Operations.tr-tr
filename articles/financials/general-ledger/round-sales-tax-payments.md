---
title: Satış vergisi ödemeleri ve yuvarlama kuralları
description: Bu makalede, Satış vergisi makamlarında yuvarlama kuralı ayarlarının nasıl çalıştığı ve Satış vergilerini kapatma ve deftere nakletme işi sırasında satış vergisi bilançosunun yuvarlanması açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1c1bb1c792eb79888a1df209f2eebaf14a38dd
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "842450"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Satış vergisi ödemeleri ve yuvarlama kuralları

[!include [banner](../includes/banner.md)]

Bu makalede, Satış vergisi makamlarında yuvarlama kuralı ayarlarının nasıl çalıştığı ve Satış vergilerini kapatma ve deftere nakletme işi sırasında satış vergisi bilançosunun yuvarlanması açıklanmaktadır.

Satış vergilerinin düzenli olarak vergi dairelerine bildirilmesi ve ödenmesi gerekir. Bu, Satış vergisi sayfasındaki satış vergisi kapatma ve nakletme işlemi çalıştırılarak yapılabilir. Bir döneme ait satış vergisi, satış vergisi hesaplarına karşı kapatılır ve satış vergisi bakiyesi Satış vergisi kapatma hesabına nakledilir. Satış verghisi kapatma hesabına nakledilen satış vergisi bakiyesi, Satş vergisi sayfasında bir yuvarlama kuralı ayarlanarak vergi kurumlarının gerektirdiği şekilde yuvarlanabilir. 

Yuvarlama farkı, Genel muhasebenin Otomatik hareketler için hesaplar alanında seçilen Satış vergisi yuvarlama hesabına nakledilir.

Aşağıdaki örnekte, Satış vergisi dairesinde yuvarlama kuralının nasıl işlediği gösterilmektedir.

## <a name="examples"></a>Örnekler

Bir döneme ilişkin toplam satış vergisi alacak bakiyesi -98.765,43 olarak görünmektedir. Tüzel kişilik ödediğinden daha fazla satış vergisi tahsil etmiştir. Bu nedenle, tüzel kişiliğin vergi dairesine ödeme yapması gerekir. 

Tüzel kişilik bakiyeyi en yakın 1,00 değerine yuvarlayan bir yuvarlama yöntemi kullanmak istemektedir. Satış vergisi muhasebesinden sorumlu kullanıcı aşağıdaki adımlardan birini gerçekleştirmelidir:

1.  Vergi &gt; Dolaylı vergiler &gt; Satış vergisi &gt; Satış vergisi dairesi öğelerine tıklayın
2.  Genel hızlı sekmesinde, Yuvarlama formu alanından Normal seçeneğini seçin.
3.  Yuvarlama alanına 1,00 girin.
4.  Satış vergisini vergi dairesine ödeme zamanı geldiğinde, Satış vergisini kapat ve naklet sayfasını açın. (Vergi &gt; Beyannameler &gt; Satış vergisi &gt; Satış vergisini kapat ve naklet'e tıklayın.)
5.  Satış vergisi kapatma hesabındaki 98.765,43 tutarındaki vergi borcu 98.765'e yuvarlanır.

Aşağıdaki tabloda, 98.765,43 tutarının Satış vergisi dairesi sayfasındaki Yuvarlama formu alanında bulunan her yuvarlama yöntemi kullanılarak nasıl yuvarlandığı gösterilmektedir.

| Yuvarlama formu seçeneği                | Yuvarlama değeri = 0,01 | Yuvarlama değeri = 0,10 | Yuvarlama değeri = 1,00 | Yuvarlama değeri = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Normal                              | 98.765,43              | 98.765,40              | 98.765,00              | 98.800,00                |
| Aşağı yuvarlama                            | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Yukarı yuvarlama                         | 98.765,43              | 98.765,50              | 98.766,00              | 98.800,00                |
| Kendi avantajı, alacak bakiyesi için | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Kendi avantajı, borç bakiyesi için  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a>Yuvarlama yok, yuvarlama 0,00 olduğundan

yuvarla(1,0151, 0,00) = 1,0151 yuvarla (1,0149, 0,00) = 1,0149

### <a name="normal-round-and-round-precision-is-001"></a>Normal yuvarlama, yuvarlama hassasiyeti 0,01'dir

<table>
  <tr>
    <td>Yuvarlama
    </td>
    <td>Hesaplama işlemi
    </td>
  </tr>
    <tr>
    <td>yuvarla(1,015, 0,01) = 1,02
    </td>
    <td>
      <ol>
        <li>yuvarla(1,015 / 0,01, 0) = yuvarla(101,5, 0) = 102
        </li>
        <li>102 * 0,01 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>yuvarla(1,014, 0,01) = 1,01
    </td>
    <td> <ol>
        <li>yuvarla(1,014 / 0,01, 0) = yuvarla(101,4, 0) = 101
        </li>
        <li>101 * 0,01 = 1,01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>yuvarla(1,011, 0,02) = 1,02
    </td>
    <td> <ol>
        <li>yuvarla(1,011 / 0,02, 0) = yuvarla(50,55, 0) = 51
        </li>
        <li>51 * 0,02 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>yuvarla(1,009, 0,02) = 1,00
    </td>
    <td> <ol>
        <li>yuvarla(1,009 / 0,02, 0) = yuvarla(50,45, 0) = 50
        </li>
        <li>50 * 0,02 = 1,00
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> Kendi avantajı seçeneğini seçerseniz, yuvarlama daima tüzel kişiliğin yararına yapılır. 

Daha fazla bilgi için aşağıdaki konulara bakın:
- [Satış vergisine genel bakış](indirect-taxes-overview.md)
- [Satış vergisi ödemesi oluşturma](tasks/create-sales-tax-payment.md)
- [Belgelerde satış hareketleri oluşturma](tasks/create-sales-tax-transactions-documents.md)
- [Deftere nakledilen satış vergisi hareketlerini görüntüleme](tasks/view-posted-sales-tax-transactions.md)
- [yuvarla işlevi](https://msdn.microsoft.com/en-us/library/aa850656.aspx)


