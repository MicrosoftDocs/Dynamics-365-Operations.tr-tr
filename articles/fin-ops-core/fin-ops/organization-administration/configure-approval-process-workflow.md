---
title: İş akışında onay işlemlerini yapılandırma
description: Onay işleminin özelliklerini yapılandırmak için aşağıdaki yordamı kullanın.
author: ChrisGarty
manager: AnnBe
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6f4f6a3fdf07ae267f92eedd312c6c721f18429
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692904"
---
# <a name="configure-approval-processes-in-a-workflow"></a>İş akışında onay işlemlerini yapılandırma

[!include [banner](../includes/banner.md)]

Onay işleminin özelliklerini yapılandırmak için aşağıdaki yordamı kullanın.

Onay işlemini yapılandırmak için iş akışı düzenleyicisinde, onay öğesine sağ tıklayın ve ardından **Özellikler** formunu açmak için **Özellikler**'e tıklayın.

## <a name="name-the-approval-process"></a>Onay işlemini adlandırma

Onay işlemi için bir ad girmek üzere aşağıdaki adımları izleyin.

1. Sol bölmede **Temel Ayarlar**'a tıklayın.
2. **Ad** alanına onay işlemi için benzersiz bir ad girin.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Sistemin ne zaman belge üzerinde otomatik olarak eylem alacağını belirtin

Sistemi belirli koşullar karşılandığında belge üstünde otomatik olarak işlem yapacak şekilde yapılandırabilirsiniz. Örneğin, sistem toplam tutarı 100 ABD Dolarından az olan gider raporlarını onaylayabilir. Sistemin belge üzerinde eylem alması gereken zamanı belirtmek için aşağıdaki adımları izleyin.

1. Sol bölmede **Otomatik eylemler**'a tıklayın.
2. **Otomatik eylemleri etkinleştir** onay kutusunu işaretleyin.
3. **Koşul ekle** seçeneğini tıklatın.
4. Koşulu girin.
5. Gerekirse başka koşullar da girin.
6. Girdiğiniz koşulların doğru biçimde yapılandırıldığını doğrulamak için aşağıdaki adımları tamamlayın:

    1. **Sınama iş akışı koşulu** formunu açmak için **Sına**'ya tıklayın.
    2. Formdaki **Koşulu doğrula** alanından bir kayıt seçin.
    3. **Sına**'ya tıklayın. Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.
    4. **Özellikler** formuna geri dönmek için **Tamam** veya **İptal**'e tıklayın.

7. **Eylemi otomatik tamamla** listesinden sistemin belge üzerinde gerçekleştirmesi gereken eylemi seçin.

## <a name="specify-when-notifications-are-sent"></a>Bildirimlerin ne zaman gönderileceğini belirtme

Bir belge onaylandığında, reddedildiğinde, temsilci atandığında, ilerletildiğinde veya bir değişiklik istendiğinde kişilere bildirim gönderebilirsiniz. Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.

1. Sol bölmede **Bildirimler**'e tıklayın.
2. Bildirim gönderilecek etkinliklerin yanındaki onay kutusunu seçin:

    - **Temsilci Seç** – Belge onay için başka kullanıcıya atandığında.
    - **İlerlet** – Atanmış kullanıcı ayrılan sürede belge üzerinde eylem gerçekleştirmediğinde.
    - **Onayla** – Belge onaylandığında.
    - **Reddet** – Belge reddedildiğinde.
    - **Değişiklik iste** – Atanmış kullanıcı gönderilmiş olan belgede bir değişiklik talep ettiğinde.

3. 2. adımda seçtiğiniz bir olay için bir satır seçin.
4. **Bildirim metni** sekmesine tıklayın.
5. Metin kutusuna bildirim için metin girin.
6. Metni kişiselleştirmek için kullanıcılara görüntülendiğinde uygun verilerle değiştirilecek yer tutucular ekleyebilirsiniz. Yer tutucu girmek için şu adımları izleyin:

    1. Yer tutucunun görünmesini istediğiniz yer için metin kutusuna tıklayın.
    2. **Yer tutucu ekle**'ye tıklayın.
    3. Görüntülenen listede, eklenecek yer tutucuyu seçin.
    4. **Ekle**'ye tıklayın.

7. Bildirimin çevirilerini eklemek için **Çeviriler**'e tıklayın. Görüntülenen formda, aşağıdaki adımları izleyin:

    1. **Ekle** seçeneğini tıklatın.
    2. Görüntülenen listede, metni gireceğiniz dili seçin.
    3. **Çevrilmiş metin** metin kutusuna metni girin.
    4. Metni kişiselleştirmek için yer tutucular ekleyin.
    5. **Kapat**'a tıklayın.

8. **Alıcı** sekmesine tıklayın.
9. Bildirimlerin gönderileceği kişiyi belirtin. Aşağıdaki tabloda seçeneklerden birini seçin ve 10. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.

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
    <td><strong>Katılımcı</strong></td>
    <td>Özel bir gruba ya da role atanmış kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Katılımcı</strong>'yı seçtikten sonra, <strong>Rol tabanlı</strong> sekmesine tıklayın.</li>
    <li><strong>Katılımcı türü</strong> listesinde, bildirimlerin gönderileceği grup türünü veya rolü seçin.</li>
    <li><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>İş akışı kullanıcısı</strong></td>
    <td>Mevcut iş akışına katılım gösteren kullanıcılar</td>
    <td>
    <ol>
    <li><strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, <strong>İş akışı kullanıcısı</strong> sekmesine tıklayın.</li>
    <li><strong>İş akışı kullanıcısı</strong> listesinde, iş akışına katılan bir kullanıcı seçin.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Kullanıcı</strong></td>
    <td>Belirli kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</li>
    <li>Bildirimlerin gönderileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. Adım 3'ten 9'a kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.

## <a name="specify-a-final-approver"></a> Son onaylayıcıyı belirtme

Onaylayanın, belgeyi onaya gönderen kişi olduğu ve "Gönderen onayına izin verme"nin kullanıldığı senaryolar için bir son onaylayan atayabilirsiniz. Son onaylayanı belirtmek için şu adımları izleyin.

1. İş akışı düzenleyicisinde, onay öğesine sağ tıklayın ve ardından **Özellikler**'i seçerek **Özellikler** formunu açın.
2. Sol bölmede **Gelişmiş ayarlar**'ı tıklatın.
3. **Son onaylayanı kullan** onay kutusunu seçin.
4. Listede, son onaylayan olacak kullanıcıyı seçin.

## <a name="set-a-time-limit"></a>Zaman limiti ayarlama

Onay işleminin belirli bir süre içerisinde tamamlanması gerekiyorsa bu adımları izleyin.

> [!NOTE]
> Bu adımlarda belirlediğiniz seçenekler her onay adımının **Atama** ve **İlerletme** alanlarında belirlediğiniz seçenekleri geçersiz kılar.

1. Sol bölmede **Gelişmiş ayarlar**'a tıklayın.
2. **İş akışı öğesi için bir zaman sınırı** **ayarlayın** onay kutusunu işaretleyin.
3. **Süre** alanında, onay işleminin ne zaman tamamlanması gerektiğini belirtin. Aşağıdaki seçeneklerden birini belirleyin:

    - **Saat** – Onay işleminin tamamlanması gereken saat sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Gün** – Onay işleminin tamamlanması gereken gün sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Hafta** – Onay işleminin tamamlanması gereken hafta sayısını girin.
    - **Ay** – Onay işleminin tamamlanmış olması gereken günü ve haftayı seçin. Örneğin onay işleminin ayın üçüncü haftasının Cuma günü tamamlanmasını isteyebilirsiniz.
    - **Yıl** – Onay işleminin tamamlanmış olması gereken günü, haftayı ve ayı seçin. Örneğin onay işleminin Aralık ayının üçüncü haftasının Cuma günü tamamlanmasını isteyebilirsiniz.

4. Zaman sınırı aşılırsa sistem belge üstünde eylem yapar. **Eylem** listesinde sistemin gerçekleştirmesi gereken eylemi seçin.

## <a name="specify-which-actions-are-available-to-the-user"></a>Hangi eylemlerin kullanıcı tarafından kullanılabilir olacağını belirtin

Bu belge onay için bir kullanıcıya atandığında kullanıcı belge üstünde işlem yapmalıdır. Kullanıcının gönderilmiş olan belge üzerinde hangi eylemleri yapabileceğini belirtmek için bu adımları izler.

1. Sol bölmede **Gelişmiş ayarlar**'a tıklayın.
2. Kullanıcı belgeyi onaylayabiliyorsa **Onayla** onay kutusunu seçin.
3. Kullanıcı belgeyi reddedebiliyorsa **Reddet** onay kutusunu seçin.
4. Kullanıcıların belgelerde değişiklik talep edebilmesi için **Değişiklik iste** onay kutusunu seçin.
5. Kullanıcı belgeyi başka bir kullanıcıya atayabilecekse **Temsilci Seç** onay kutusunu işaretleyin.

> [!NOTE]
> **Kurumsal Portal içindeki iş listesinden eylemleri etkinleştir** onay kutusu kullanımdan kaldırılmıştır.

## <a name="configure-the-approval-steps"></a> Onay adımlarını yapılandırma

Onay işlemi onay adımlarından oluşur. Onay işlemine adım eklemek ve adımları yapılandırmak için aşağıdaki yordamı tamamlayın.

1. İş akışı düzenleyicisinde onay işlemine çift tıklayın. İş akışı düzenleyicisi onay işleminin adımlarını görüntüler.
2. Onay adımı eklemek için adımları **İş akışı öğeleri** alanından tuvale sürükleyin.
3. Onay adımını yapılandırmak için bkz. [İş akışında onay adımlarını yapılandırma](configure-approval-step-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]