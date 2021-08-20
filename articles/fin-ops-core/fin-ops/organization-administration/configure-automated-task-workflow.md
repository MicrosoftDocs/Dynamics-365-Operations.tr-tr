---
title: İş akışında otomatikleştirilmiş görevleri yapılandırma
description: Bu konu, otomatik bir görevin özelliklerini yapılandırmayı açıklar.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0cc7097d956b0fabdc8cf16cfb99b065e3e03f21e9cfd56c4b4b91930dbef2b7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764395"
---
# <a name="configure-automated-tasks-in-a-workflow"></a>İş akışında otomatikleştirilmiş görevleri yapılandırma

[!include [banner](../includes/banner.md)]

Bu konu, otomatik bir görevin özelliklerini yapılandırmayı açıklar.

Otomatik bir görevi iş akışı düzenleyicisinde yapılandırmak için göreve sağ tıklatın ve sonra **Özellikler**'i açmak için **Özellikler** sayfanı tıklayın. Ardından otomatik görevin özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.

## <a name="name-the-task"></a>Görevi adlandırma

Otomatik göreve bir ad vermek için aşağıdaki adımları takip edin.

1. Sol bölmede **Temel Ayarlar**'ı tıklatın.
2. **Ad** alanına görev için benzersiz bir ad girin.

## <a name="specify-when-notifications-are-sent"></a>Bildirimlerin ne zaman gönderileceğini belirtme

Otomatik bir görev çalıştırıldığında veya iptal edildiğinde insanlara bildirimler gönderebilirsiniz. Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.

1. Sol bölmede **Bildirimler**'i tıklatın.
2. Bildirim gönderilecek etkinliklerin yanındaki onay kutusunu seçin:

    - **Yürütme** – Görev çalıştırıldığında bildirim gönderilir.
    - **İptal Edildi** – Görev iptal edildiğinde bildirim gönderilir.

3. 2. adımda seçtiğiniz bir olay için bir satır seçin.
4. **Bildirim metni** sekmesinde, metin kutusuna, bildirimin metnini girin.
5. Bildirimi kişiselleştirmek için yer tutucular ekleyebilirsiniz. Yer tutucular, bildirim kullanıcılara gösterildiğinde uygun verilerle değiştirilir. Yer tutucu eklemek için şu adımları izleyin:

    1. Metin kutusunda, yer tutucunun görüneceği yere tıklayın.
    2. **Yer tutucu ekle**'yi tıklatın.
    3. Beliren listede, eklenecek yer tutucuyu seçin.
    4. **Ekle**'yi tıklatın.

6. Bildirimin çevirilerini eklemek için şu adımları izleyin:

    1. **Çeviriler**'e tıklayın.
    2. Beliren sayfada **Ekle**'yi tıklatın.
    3. Beliren listede, metni girdiğiniz dili seçin.
    4. **Çevrilen metin** alanında, metni girin.
    5. Metni kişiselleştirmek için, 5. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.
    6. **Kapat** düğmesini tıklayın.

7. **Alıcı** sekmesinde, bildirimlerin kime gönderildiğini belirtin. Aşağıdaki tablodaki seçeneklerden birini seçin ve 8. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.

    <table>
    <thead>
    <tr>
    <th>Seçenek</th>
    <th>Bildirim alıcıları</th>
    <th>Ek adımlar</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Katılımcı</td>
    <td>Özel bir gruba ya da role atanmış kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, bildirimlerin gönderileceği grup ya da rolün türünü seçin.</li>
    <li><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>İş akışı kullanıcısı</td>
    <td>Mevcut iş akışına katılım gösteren kullanıcılar</td>
    <td>
    <ul>
    <li><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Kullanıcı</td>
    <td>Belirli kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</li>
    <li><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm  kullanıcılarını içerir. Bildirimlerin gönderileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]