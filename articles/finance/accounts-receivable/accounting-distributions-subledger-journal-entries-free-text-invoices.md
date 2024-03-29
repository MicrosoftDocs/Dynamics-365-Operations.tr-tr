---
title: Serbest metin faturalar için muhasebe dağılımları ve günlük girişleri
description: Muhasebe dağılımları, bir tutarın, örneğin gelirin, verginin veya masrafların bir serbest metin faturasında nasıl hesaba katılacağını tanımlamak için kullanılır. Serbest metin faturası günlüğe kaydedildiğinde hesaba katılması gereken tüm tutarlar, bir veya daha fazla muhasebe dağıtımına sahip olacaktır.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5120c4e75e821776201d5add2d498feb94d0297
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778424"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a>Serbest metin faturaları için muhasebe dağılımları ve yardımcı defter girişleri

[!include [banner](../includes/banner.md)]

Muhasebe dağılımları, bir tutarın, örneğin gelirin, verginin veya masrafların bir serbest metin faturasında nasıl hesaba katılacağını tanımlamak için kullanılır. Serbest metin faturası günlüğe kaydedildiğinde hesaba katılması gereken tüm tutarlar, bir veya daha fazla muhasebe dağıtımına sahip olacaktır.

## <a name="accounting-distributions"></a>Muhasebe dağıtımları

**Serbest metin faturası** sayfasında aşağıdaki düğmeleri kullanarak serbest metin faturası üzerindeki her bir satır için muhasebe dağılımlarını görüntüleyebilir ve değiştirebilirsiniz

-   **Tutarları dağıtmak**—Vergiler ve masraflar gibi tek bir satır ve tüm alt satırların muhasebe dağılımlarını görüntüleyip, değiştirin. Alt satır için muhasebe dağılımlarını da doğrudan **Satış vergisi hareketleri** sayfasından veya **Gider hareketleri** sayfasından görüntüleyebilir ve değiştirebilirsiniz.
    -   Serbest metin faturası başlığındaki tutarlar, örneğin gider veya para birimi yuvarlama tutarlarını, değiştirin.
    -   Serbest metin faturası satır tutarlarını değiştirme
-   **Dağılımları görüntülemek**— Belge üzerindeki tüm satırların muhasebe dağılımlarını görüntüleyin. Muhasebe dağılımlarını bu görünümden değiştiremezsiniz.
    -   Başlığı ve satır tutarlarını görüntüleyin.

## <a name="distributing-amounts"></a>Dağılım tutarları
Serbest metin faturası girdiğinizde, her tutar aşağıdaki şekilde dağılır.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Parasal tutarın türü</th>
<th>Ana hesabın nereden görüntüleneceği</th>
<th>Hangi varsayılan mali boyutun görüntüleneceğini belirleyen öncelik sırası</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Serbest metin faturası satırı</td>
<td>Serbest metin fatura satırındaki genel muhasebe hesabı.</td>
<td><ol>
<li>Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</li>
<li>Ana hesap tahsisat hesabı değilse, serbest metin faturası satırındaki mali boyut varsayılan şablonunu kullanın.</li>
<li>Serbest metin faturası satırındaki varsayılan mali boyut değerlerini kullanın.</li>
<li>Hesap planı sayfasındaki genel muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="even">
<td>Sabit kıymet numarası ve değer modeli birleşimi için serbest metinli fatura satırı
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Not </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Serbest metin faturası satırındaki ana hesap, sabit kıymet elden hesabı olacaktır.</td>
</tr>
</tbody>
</table>
</div></td>
<td>Serbest metin fatura satırındaki genel muhasebe hesabı.</td>
<td><ol>
<li>Serbest metin faturası satırındaki varsayılan mali boyut değerlerini kullanın.</li>
<li>Hesap planı sayfasındaki genel muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Serbest metinli fatura iskonto tutarı</td>
<td>Nakit iskontoları sayfasındaki Müşteri iskontoları alanı için ana hesap.</td>
<td><ol>
<li>Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</li>
<li>Ana hesap tahsisat hesabı değilse, serbest metin faturası satırındaki mali boyut varsayılan şablonunu kullanın.</li>
<li>Serbest metin faturası satırındaki varsayılan mali boyut değerlerini kullanın.</li>
<li>Hesap planı sayfasındaki genel muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="even">
<td>Serbest metin faturası satış vergisi tutarı</td>
<td>Genel muhasebe deftere nakil grupları sayfasındaki satış vergisi borcu alanı.</td>
<td><ol>
<li>Serbest metin faturası satır tutarında veya satır tutarı dağıtım giderinde tanımlanan mali boyutları kullanın.</li>
<li>Serbest metin faturası satırındaki varsayılan mali boyut değerlerini kullanın.</li>
<li>Hesap planı sayfasındaki genel muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Serbest metin faturası masraf satır tutarı</td>
<td>Masraflar kodu sayfasındaki alacak hesabı alanı.</td>
<td><ol>
<li>Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</li>
<li>Ana hesap tahsisat hesabı değilse, serbest metin faturası satırındaki mali boyut varsayılan şablonunu kullanın.</li>
<li>Serbest metin faturası satırındaki varsayılan mali boyut değerlerini kullanın.</li>
<li>Hesap planı sayfasındaki genel muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Vergileri dağıtma
Vergiler için muhasebe dağılımları, vergiler hesaplanana dek oluşturulamaz. Satış vergilerini hesaplamak için **serbest metin faturası** sayfasında aşağıdaki görevleri tamamlamanız gerekir:
-   Satış vergisini görüntüleyin.
-   Fatura toplamını görüntüleyin.
-   Nakit akışı tahminini görüntüleyin.
-   Serbest metin faturasının tamamının içindeki muhasebe dağılımlarını görüntüleyin.
-   Yardımcı defter günlüğünü görüntüleyin.

## <a name="subledger-journals-for-free-text-invoices"></a>Serbest metin faturaları için muavin defter günlükleri
Tam bir serbest metin faturasını deftere nakletmeden önce, faturanın doğru hesaplara nakledildiğini teyit etmek için, borçlar ve alacaklar dahil, faturanun tüm muhasebe girdisini görebilirsiniz. Bu tam görünümün muavin defteri günlük hesap girişi olarak adlandırılır. Serbest metin faturasını günlüğe geçirmeden önce önizlemesini görüntülediğinizde muavin defteri günlük girdisi yanlış ise, muavin defteri günlük girdisi değiştiremezsiniz. Bunun yerine, hesap dağıtımları veya deftere nakil profili değiştirmeniz gerekir. Hesap dağıtımları muhasebe girişi, Borç veya alacak bir tarafı tanımlamak için kullanılır. Muavin defteri günlük mahsuplaştırma hesabı girişi deftere nakil profilleri gibi müşteri hesabı ya da vergi oluşturulur.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
