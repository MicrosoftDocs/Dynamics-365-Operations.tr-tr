---
title: Tahakkuk eden abonelikler
description: Servis abonelikleriyle, işlem harcını faturaladığınız tarihi izleyen dönemlerde geliri el ile tahakkuk ettirebilirsiniz.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d6f2f69b7093e5408b016f4a69792b28c70f57f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824690"
---
# <a name="accruing-subscriptions"></a>Tahakkuk eden abonelikler 

[!include [banner](../includes/banner.md)]


Servis abonelikleriyle, işlem harcını faturaladığınız tarihi izleyen dönemlerde geliri el ile tahakkuk ettirebilirsiniz.

Abonelik ücreti için ayarladığınız fatura dönemi için tahakkuk dönemleri oluşturulur, ve tahakkuk dönemlerinde aboneliğin dönem kodu temel alınır.

Geliri tahakkuk ettirebilir ve tahakkuk eden geliri ters kaydedebilirsiniz.

## <a name="reverse-accruals-of-credit-amounts"></a>Alacak tutarlarına ters tahakkuk işlemi uygulama

Faturalanmış abonelik tutarlarını alacaklandırabilir, tahakkuk eden tutarlara ters işlem uygulamak için iki yöntem kullanabilirsiniz:

  - Hareket için bir alacak dekont teklifi oluşturmadan önce her tahakkuk eden gelir hareketini el ile ters kaydedebilirsiniz. Bu, el ile yöntemidir. (el ile)

  - Alacak dekontunun deftere nakledildiği tarihte veya tahakkukun orijinal deftere nakil tarihinde tahakkuk eden tutarlara tersine işlem uygulayabilirsiniz.

Daha fazla bilgi için bkz. [Abonelik parametreleri (form)](https://technet.microsoft.com/library/aa619615.aspx).

## <a name="setup-requirements"></a>Gereksinimler kurulumu

Geliri tahakkuk ettirmek için, aşağıdaki veri gereksinimlerinin karşılandığından emin olun.

## <a name="account-setup"></a>Hesap kurulumu

**Proje** modülünde **Süren İş - abonelik** ve **Tahakkuk eden gelir - abonelik** hesapları ayarlanmalıdır.

Tahakkuk eden geliri deftere naklettiğinizde, **Süren iş - abonelik** hesabı tahakkuk tutarında borçlandırılır ve **Tahakkuk eden gelir - abonelik** hesabı tahakkuk tutarında alacaklandırılır.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Abonelik gelirinin tahakkuku için hesapların kurulumu

1.  **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Deftere nakil** \> **Genel muhasebe deftere nakil ayarı**'na tıklayın.

2.  **Gelir hesapları** sekmesine tıklayın, **Süren iş - abonelik** veya **Tahakkuk eden gelir - abonelik** seçeneğini belirterek hesapları ayarlayın.

## <a name="subscription-group-setup"></a>Abonelik grubu kurulumu

Abonelikler için gelir tahakkuku yapabilmek için **Gelir tahakkuku** onay kutusunun seçilmiş olması gerekir. Bu, aboneliğe eklenmiş gruba yönelik **Abonelik grupları** formunda bulunur. **Hizmet yönetimi** \> **Kurulum** \> **Servis abonelikleri** \> **Abonelik grupları**'na tıklayın.

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Abonelik grubunda gelir tahakkukunu etkinleştirme

1.  **Hizmet yönetimi** \> **Kurulum** \> **Servis abonelikleri** \> **Abonelik grupları**'na tıklayın.

## <a name="periods"></a>Dönemler

Faturalama dönem kodunu ayarlamanız gerekir. Gelirin, faturalama için kullandığınız zaman aralığı içinde tahakkuk edilmesini istemediğiniz sürece, tahakkuk dönemini ayarlamalısınız.

Aşağıdaki tablo, hangi faturalama dönemleri için hangi tahakkuk dönemlerini ayarlayabileceğinize ilişkin genel bir fikir sağlar:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Faturalama dönemi</p></th>
<th><p>Tahakkuk dönemi</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Yıllar</strong></p></td>
<td><ul>
<li><p><strong>Yıllar</strong></p></li>
<li><p><strong>Üç aylık dönem</strong></p></li>
<li><p><strong>Ay</strong></p></li>
<li><p><strong>Gün</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Üç aylık dönem</strong></p></td>
<td><ul>
<li><p><strong>Üç aylık dönem</strong></p></li>
<li><p><strong>Ay</strong></p></li>
<li><p><strong>Gün</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Ay</strong></p></td>
<td><ul>
<li><p><strong>Ay</strong></p></li>
<li><p><strong>Gün</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Hafta</strong></p></td>
<td><ul>
<li><p><strong>Gün</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Gün</strong></p></td>
<td><ul>
<li><p><strong>Gün</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

Fatura dönemini ayarlama genel abonelik grubu kurulumunun zorunlu bir parçasıdır. Ayrıca abonelik grubu için bir tahakkuk dönemi ayarlamak isteyip istemediğinize karar verebilirsiniz. Abonelik grubu için tahakkuk dönemi ayarlarsanız, bu dönem **Dönem kodu** alanında önerilir. Bu alan, abonelik geliri tahakkuk ettirdiğinizde **Abonelik Geliri Tahakkuku** formunda yer alır. Bununla birlikte, tahakkuk dönemi abonelik grubu hakkında isteğe bağlı bir bilgidir.


> [!NOTE]
> <P><STRONG>Abonelik geliri tahakkuku</STRONG> formunu açmak için aşağıdaki yolu kullanın. <STRONG>Hizmet yönetimi</STRONG> &gt; <STRONG>Periyodik</STRONG> &gt; <STRONG>Servis abonelikleri</STRONG> &gt; <STRONG>Abonelik geliri tahakkuku</STRONG>'na tıklayın.</P>


## <a name="transactions"></a>Hareketler

Tahakkuk eden geliri deftere naklederken oluşturulan genel muhasebe hareketlerinin sayısı denetleyebilirsiniz. Aboneliklerde, genel muhasebe hareketlerinin toplam olarak mı yoksa satır başına olarak mı oluşturulacağını tanımlayın.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Tahakkuk eden hareketler için görüntülenecek deftere nakil ayrıntılarının düzeyini belirleme

1.  **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri**'ne tıklayın.

2.  **Mali** sekmesinde, **Fatura** alanında, **Toplam** veya **Satır** seçeneğini belirleyin.


## <a name="see-also"></a>Ayrıca bkz.

[Abonelik geliri tahakkuku](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]