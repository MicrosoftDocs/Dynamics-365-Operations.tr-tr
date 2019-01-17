---
title: "İş akışı özelliklerini yapılandırma"
description: "Bu konu İş akışının çeşitli özelliklerini yapılandırmayı açıklar."
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 576ce368b2a8672aa39116eb0cc6e3d3f2a06bb3
ms.contentlocale: tr-tr
ms.lasthandoff: 12/18/2018

---

# <a name="configure-workflow-properties"></a>İş akışı özelliklerini yapılandırma

[!include [banner](../includes/banner.md)]

Bu konu İş akışının çeşitli özelliklerini yapılandırmayı açıklar.

Bir iş akışının özelliklerini yapılandırmak için iş akışını, iş akışı düzenleyicisinde açın. İş akışı düzenleyicisinin tuvaline tıklayın ve sonra **Seçenekler**'e tıklayarak **Özellikler** sayfasını açın. Daha sonra aşağıdaki yordamları kullanarak iş akışının çeşitli özelliklerini yapılandırabilirsiniz.

## <a name="name-the-workflow"></a>İş akışını adlandırma

İş akışı için bir ad girmek üzere şu adımları izleyin.

1. Sol bölmede **Temel Ayarlar**'ı tıklatın.
2. **Adı** alanına iş akışı için benzersiz bir ad girin. Örneğin, faaliyet göstermekte olduğunuz her ülke/bölge için bir satınalma talebi iş akışı oluşturursanız, satınalma talebi iş akışını **Satınalma Talepleri Danimarka** veya **Satınalma Talepleri İspanya** olarak adlandırabilirsiniz.

## <a name="specify-the-workflow-owner"></a>İş akışı sahibini belirtme

İş akışının sahibi, ilgili iş akışını yönetecek ve bakımını yapacak olan kişidir. İş akışı sahibini belirtmek için şu adımları izleyin.

1. Sol bölmede **Temel Ayarlar**'ı tıklatın.
2. **Sahibi** listesinde, iş akışını yönetecek olan kişinin adını seçin.

## <a name="select-an-email-template"></a>Bir e-posta şablonu seçin

İş akışı hakkında bildirim iletilerini oluşturmakta kullanılacak e-posta şablonunu seçmek için aşağıdaki adımları izleyin.

1. Sol bölmede **Temel Ayarlar**'ı tıklatın.
2. **İş akışı bildirimleri için e-posta şablonu** listesinde, şablonu seçin.

## <a name="enter-instructions-for-users"></a>Kullanıcılar için yönergeler girme

İşlenmek ve onaylanmak üzere belgeler gönderen kullanıcılara yönergeler sağlayabilirsiniz. Bu kullanıcılar ayrıca *oluşturucular* olarak adlandırılır. Örneğin, bir satınalma talebi iş akışı oluşturuyorsunuz ve yönergeleri giriyorsunuz. Bu yönergeler daha sonra satınalma taleplerini **Satınalma talepleri** sayfasına giren kullanıcılar tarafından görüntülenebilir. Oluşturucu, yönergeleri görüntülemek için iş akışı ileti çubuğundaki simgeye tıklar. Kullanıcılar için yönergeler girmek üzere şu adımları izleyin.

1. Sol bölmede **Temel Ayarlar**'ı tıklatın.
2. **Gönderim yönergeleri** alanında, yönergeleri girin.
3. Yönergeleri kişiselleştirmek için, yer tutucular ekleyebilirsiniz. Yer tutucular, yönergeler kullanıcılara gösterildiğinde uygun verilerle değiştirilir. Yer tutucu girmek için şu adımları izleyin:

    1. Yer tutucunun görünmesini istediğiniz yeri belirtmek üzere **Gönderi yönergeleri** alanını tıklatın.
    2. **Yer tutucu ekle**'yi tıklatın.
    3. Beliren listede, eklenecek yer tutucuyu seçin.
    4. **Ekle**'yi tıklatın.

4. Yönergelerin çevirilerini eklemek için şu adımları izleyin:

    1. **Çeviriler**'e tıklayın.
    2. Beliren sayfada **Ekle**'yi tıklatın.
    3. Beliren listede, metni gireceğiniz dili seçin.
    4. **Çevrilen metin** alanında, metni girin.
    5. Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz. Yer tutucu girmek hakkında yönergeler için, adım 3'e bakın.
    6. **Kapat** düğmesini tıklayın.

## <a name="specify-when-this-workflow-is-used"></a>Bu iş akışının ne zaman kullanılacağını belirtin

Aynı türe dayalı birden çok iş akışı oluşturabilirsiniz. Örneğin, faaliyet gösterdiğiniz her ülke/bölge için bir satınalma talebi iş akışı oluşturabilirsiniz, örneğin Satınalma Talepleri Danimarka ve Satınalma Talepleri İspanya gibi. Aynı türe dayalı birden çok iş akışınız olduğunda, her bir iş akışının ne zaman kullanıldığını belirtmelisiniz. Önceki örnek için, aşağıdaki koşulları belirtebilirsiniz:

- Satınalma Talebi Danimarka: ülke/bölge = DK olduğunda kullanılır
- Satınalma Talebi İspanya: ülke/bölge = ES olduğunda kullanılır

Yapılandırmakta olduğunuz iş akışının ne zaman kullanılacağını belirtmek için şu adımları izleyin.

1. Sol bölmede **Etkinleştirme**'yı tıklatın.
2. **Bu iş akışını çalıştırmak için koşullar** onay kutusunu seçin.
3. **Koşul ekle** seçeneğini tıklatın.
4. Koşulu girin.
5. Varsa, gerekli ek koşulları girin.
6. Girdiğiniz koşulların doğru biçimde ayarlandığını doğrulamak için, aşağıdaki adımları izleyin:

    1. **Sına**'yı tıklatın.
    2. **İş akışını test et** sayfasında, **Koşulu doğrula** alanında, bir kayıt seçin.
    3. **Sına**'yı tıklatın. Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir. Örneğin, İspanya için bir satınalma talebi iş akışı oluşturuyorsanız, sayfanın **Koşulu doğrula** bölgesi satınalma taleplerinin bir listesini gösterir. **Sına**'yı tıklattığınızda, sistem seçili olan satınalma talebini değerlendirir ve ülke/bölgenin olarak ES olup olmadığını belirler.
    4. **Özellikler** sayfasında geri dönmek için **OK** ya da **İptal Et**'e tıklayın.

## <a name="specify-when-notifications-are-sent"></a>Bildirimlerin ne zaman gönderileceğini belirtme

Bir belge işlenmek üzere gönderildiğinde, bir iş akışı örneği oluşturulur. Bu iş akışını temel alan iş akışı örnekleri başlatıldığında, sona erdirildiğinde, bitirildiğinde veya bir hata nedeniyle durdurulduğunda kullanıcılara bildirimler gönderebilirsiniz. Bildirimlerin ne zaman gönderileceğini belirtmek için şu adımları izleyin.

1. Sol bölmede **Bildirimler**'i tıklatın.
2. Bildirimleri tetiklemesi gereken her olay için onay kutusunu seçin:

    - **Başlatıldı** — Bir iş akışı örneği başlatıldığında bildirim gönder.
    - **Durduruldu** — İş akışı örneği oluşan bir hata nedeniyle durdurulduğunda bildirimler gönder.
    - **Tamamlandı** — Bir iş akışı örneği tamamlandığında bildirim gönder.
    - **Kurtarılamaz** — İş akışı örneği oluşan kurtarılamaz bir hata nedeniyle durdurulduğunda bildirimler gönder.
    - **Sona erdirildi** — Bir iş akışı örneği sone erdirildiğinde bildirim gönder.

3. 2. adımda seçtiğiniz bir olay için bir satır seçin.
4. **Bildirim metni** sekmesinde bildirimin metnini girin.
5. Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz. Yer tutucular, metin kullanıcılara gösterildiğinde uygun verilerle değiştirilir. Yer tutucu girmek için şu adımları izleyin:

    1. Yer tutucunun görünmesini istediğiniz yeri belirtmek üzere alan içerisine tıklatın.
    2. **Yer tutucu ekle**'yi tıklatın.
    3. Beliren listede, eklenecek yer tutucuyu seçin.
    4. **Ekle**'yi tıklatın.
    5. Eklenecek ortak **Bildirim metni** yer tutucusu önceki adımdaki yorumları görüntüleyen "Son Notlar: %Workflow.Last note%" öğesidir.

6. Metnin çevirilerini eklemek için şu adımları izleyin:

    1. **Çeviriler**'e tıklayın.
    2. Beliren sayfada **Ekle**'yi tıklatın.
    3. Beliren listede, metni gireceğiniz dili seçin.
    4. **Çevrilen metin** alanında, metni girin.
    5. Metni kişiselleştirmek için, yer tutucular ekleyebilirsiniz. Yer tutucu girmek hakkında yönergeler için, adım 5'e bakın.
    6. **Kapat** düğmesini tıklayın.

7. **Alıcı** sekmesinde, aşağıdaki seçenekleri kimin bildirim alacağını belirtmek için kullanın.

    <table>
    <thead>
    <tr>
    <th>Seçenek</th>
    <th>Bildirimler bu kullanıcılara gönderilir.</th>
    <th>Bildirimleri göndermek için aşağıdaki adımları izleyin</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Katılımcı</td>
    <td>Özel bir gruba ya da role atanmış kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Alıcı</strong> sekmesinde, <strong>Katılımcı</strong>'yı tıklatın.</li>
    <li><strong>Rol tabanlı</strong> sekmesindeki <strong>Katılımcı türü</strong> listesinde, bildirimin gönderileceği grup türünü veya rolünü seçin.</li>
    <li><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>İş akışı kullanıcısı</td>
    <td>Bu iş akışında katılımcı olan kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Alıcı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı tıklatın.</li>
    <li><strong>İş akışı kullanıcısı</strong> sekmesindeki <strong>İş akışı kullanıcısı</strong> listesinden, bu iş akışının bir katılımcısını seçin.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Kullanıcı</td>
    <td>Belirli Finance and Operations kullanıcıları</td>
    <td>
    <ol>
    <li><strong>Alıcı</strong> sekmesinde, <strong>Kullanıcı</strong>'yı tıklatın.</li>
    <li><strong>Kullanıcı</strong> sekmesindeki <strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Finance and Operations kullanıcılarını içerir. Bildirimlerin gönderileceği kullanıcıları seçin ve bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>İş akışında yaptığınız değişiklikler hakkında açıklamalar girin

İş akışında yaptığınız değişiklikler hakkında açıklamalar girmek için şu adımları izleyin.

1. Sol bölmede **Notlar**'u tıklatın.
2. **İş akışı hakkında yorumlar girin** alanında, yorumlarınızı girin.
3. Yorumlarınızı gözden geçirin. Yorumlarınızı ekledikten sonra üzerlerinde değişiklik yapamazsınız.
4. **Yorum geçmişi** alanına yorumlarınızı eklemek için **Ekle**'yi tıklatın.

