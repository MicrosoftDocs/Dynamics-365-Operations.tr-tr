---
title: Tahakkuk eden abonelikler
description: Servis abonelikleriyle, işlem harcını faturaladığınız tarihi izleyen dönemlerde geliri el ile tahakkuk ettirebilirsiniz.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ff184b24a264e37613b2302a3d92b74e870c5ac
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677352"
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

Daha fazla bilgi için bkz. [Abonelik parametreleri (form)](/dynamicsax-2012//subscription-parameters-form).

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

**Hizmet yönetimi** \> **Kurulum** \> **Servis abonelikleri** \> **Abonelik grupları**'na tıklayın.

## <a name="periods"></a>Dönemler

Faturalama dönem kodunu ayarlamanız gerekir. Gelirin, faturalama için kullandığınız zaman aralığı içinde tahakkuk edilmesini istemediğiniz sürece, tahakkuk dönemini ayarlamalısınız.

Aşağıdaki tablo, hangi faturalama dönemleri için hangi tahakkuk dönemlerini ayarlayabileceğinize ilişkin genel bir fikir sağlar:

<table>
<colgroup>
<col />
<col />
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