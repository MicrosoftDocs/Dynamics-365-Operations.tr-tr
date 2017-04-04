---
title: "İş akışı içinde bir onay işlemi yapılandırma"
description: "Onay işleminin özelliklerini yapılandırmak için aşağıdaki yordamı kullanın."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 579e393ef64bc5ad72d129ac08ac215c524d5c55
ms.lasthandoff: 03/31/2017


---

# <a name="configure-an-approval-process-in-a-workflow"></a>İş akışı içinde bir onay işlemi yapılandırma

Onay işleminin özelliklerini yapılandırmak için aşağıdaki yordamı kullanın.

İş akışı düzenleyicisinde bir onay işlemini yapılandırmak için onay öğeye sağ tıklayın ve sonra **Özellikler** açmak için **Özellikler** formu.
Onay işlemini adlandırma
-------------------------

Onay işlemi için bir ad girmek üzere aşağıdaki adımları izleyin.
1.  Sol bölmede **Temel Ayarlar**'a tıklayın.
2.  **Ad** alanına onay işlemi için benzersiz bir ad girin.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Sistemin ne zaman belge üzerinde otomatik olarak eylem alacağını belirtin
Sistemi belirli koşullar karşılandığında belge üstünde otomatik olarak işlem yapacak şekilde yapılandırabilirsiniz. Örneğin, sistem toplam tutarı 100 ABD Dolarından az olan gider raporlarını onaylayabilir. Sistemin belge üzerinde eylem alması gereken zamanı belirtmek için aşağıdaki adımları izleyin.
1.  Sol bölmede **Otomatik eylemler**'a tıklayın.
2.  **Otomatik eylemleri etkinleştir** onay kutusunu işaretleyin.
3.  Click **Add condition**.
4.  Koşulu girin.
5.  Gerekirse başka koşullar da girin.
6.  Girdiğiniz koşulların doğru biçimde yapılandırıldığını doğrulamak için aşağıdaki adımları tamamlayın:
    1.  **Sınama iş akışı koşulu** formunu açmak için **Sına**'ya tıklayın.
    2.  Formdaki **Koşulu doğrula** alanından bir kayıt seçin.
    3.  **Sına**'ya tıklayın. Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.
    4.  ' I **Tamam** veya **iptal** dönmek için **Özellikler** formu.

7.  **Eylemi otomatik tamamla** listesinden sistemin belge üzerinde gerçekleştirmesi gereken eylemi seçin.

## <a name="specify-when-notifications-are-sent"></a>Bildirimlerin ne zaman gönderileceğini belirtme
Bir belge onaylandığında, reddedildiğinde, temsilci atandığında, ilerletildiğinde veya bir değişiklik istendiğinde kişilere bildirim gönderebilirsiniz. Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.
1.  Sol bölmede **Bildirimler**'e tıklayın.
2.  Bildirim gönderilecek etkinliklerin yanındaki onay kutusunu seçin:
    -   **Temsilci** – bir belgeyi onay için başka bir kullanıcıya atandığında.
    -   **İlerlet** – zaman atanan kullanıcı bir belge üzerinde ayrılan sürede hedefler değil.
    -   **Onaylama** – bir belge onaylandığında.
    -   **Reddetme** – bir belge reddedildiğinde.
    -   **Değişiklik iste** – gönderilen bir belgede atanan kullanıcının istediği zaman.

3.  2. adımda seçtiğiniz bir olay için bir satır seçin.
4.  **Bildirim metni** sekmesine tıklayın.
5.  Metin kutusuna bildirim için metin girin.
6.  Metni kişiselleştirmek için kullanıcılara görüntülendiğinde uygun verilerle değiştirilecek yer tutucular ekleyebilirsiniz. Yer tutucu girmek için şu adımları izleyin:
    1.  Yer tutucunun görünmesini istediğiniz yer için metin kutusuna tıklayın.
    2.  **Yer tutucu ekle**'ye tıklayın.
    3.  Görüntülenen listede, eklenecek yer tutucuyu seçin.
    4.  **Ekle**'ye tıklayın.

7.  Bildirimin Çeviriler eklemek için tıklatın **çevirileri**. Görüntülenen formda, aşağıdaki adımları izleyin:
    1.  Click **Add**.
    2.  Görüntülenen listede, metni gireceğiniz dili seçin.
    3.  **Çevrilmiş metin** metin kutusuna metni girin.
    4.  Metni kişiselleştirmek için yer tutucular ekleyin.
    5.  **Kapat**'a tıklayın.

8.  **Alıcı** sekmesine tıklayın.
9.  Bildirimlerin gönderileceği kişiyi belirtin. Aşağıdaki tabloda seçeneklerden birini seçin ve 10. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Seçenek</th>
    <th>Bildirim alıcıları</th>
    <th>Ek adımlar</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>Katılımcı</strong></td>
    <td>Özel bir gruba ya da role atanmış kullanıcılar</td>
    <td><ol>
    <li><strong>Katılımcı</strong>'yı seçtikten sonra, <strong>Rol tabanlı</strong> sekmesine tıklayın.</li>
    <li><strong>Katılımcı türü</strong> listesinde, bildirimlerin gönderileceği grup türünü veya rolü seçin.</li>
    <li><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><strong>İş akışı kullanıcısı</strong></td>
    <td>Mevcut iş akışına katılım gösteren kullanıcılar</td>
    <td><ol>
    <li><strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, <strong>İş akışı kullanıcısı</strong> sekmesine tıklayın.</li>
    <li><strong>İş akışı kullanıcısı</strong> listesinde, iş akışına katılan bir kullanıcı seçin.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><strong>User</strong></td>
    <td>İşlemleri kullanıcılar için belirli Microsoft Dynamics 365</td>
    <td><ol>
    <li><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</li>
    <li><strong>Kullanılabilir kullanıcılar</strong>: tüm Microsoft Dynamics 365 işlemlerini kullanıcılar için liste içerir. Bildirimlerin gönderileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar:</strong> listesine taşıyın.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. Adım 3'ten 9'a kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.

## <a name="specify-a-final-approver"></a> Son onaylayıcıyı belirtme
Onaylayanın belgeyi onay için gönderen kişi olduğu senaryolar için son onaylayan atayabilirsiniz. Son onaylayanı belirtmek için şu adımları izleyin.
1.  Sol bölmede **Gelişmiş ayarlar**'a tıklayın.
2.  **Son onaylayanı kullan** onay kutusunu seçin.
3.  Listede, son onaylayan olacak kullanıcıyı seçin.

## <a name="set-a-time-limit"></a>Zaman limiti ayarlama
Onay işleminin belirli bir süre içerisinde tamamlanması gerekiyorsa bu adımları izleyin.
| **Not **                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bu adımlarda belirlediğiniz seçenekler her onay adımının **Atama** ve **İlerletme** alanlarında belirlediğiniz seçenekleri geçersiz kılar. |

1.  Sol bölmede **Gelişmiş ayarlar**'a tıklayın.
2.  **İş akışı öğesi için bir zaman sınırı** **ayarlayın** onay kutusunu işaretleyin.
3.  **Süre** alanında, onay işleminin ne zaman tamamlanması gerektiğini belirtin. Aşağıdaki seçeneklerden birini belirleyin:
    -   **Saat** – Onay işleminin tamamlanması gereken saat sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    -   **Gün** – Onay işleminin tamamlanması gereken gün sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    -   **Hafta** – Onay işleminin tamamlanması gereken hafta sayısını girin.
    -   **Ay** – Onay işleminin tamamlanmış olması gereken günü ve haftayı seçin. Örneğin onay işleminin ayın üçüncü haftasının Cuma günü tamamlanmasını isteyebilirsiniz.
    -   **Yıl** – Onay işleminin tamamlanmış olması gereken günü, haftayı ve ayı seçin. Örneğin onay işleminin Aralık ayının üçüncü haftasının Cuma günü tamamlanmasını isteyebilirsiniz.

4.  Zaman sınırı aşılırsa sistem belge üstünde eylem yapar. **Eylem** listesinde sistemin gerçekleştirmesi gereken eylemi seçin.

## <a name="specify-which-actions-are-available-to-the-user"></a>Hangi eylemlerin kullanıcı tarafından kullanılabilir olacağını belirtin
Bu belge onay için bir kullanıcıya atandığında kullanıcı belge üstünde işlem yapmalıdır. Kullanıcının gönderilmiş olan belge üzerinde hangi eylemleri yapabileceğini belirtmek için bu adımları izler.
1.  Sol bölmede **Gelişmiş ayarlar**'a tıklayın.
2.  Seçin **Onayla** kullanıcı belgeyi onaylamak için kullanabileceğiniz onay kutusunu.
3.  Seçin **reddetme** onay kutusunu kullanıcı belgeyi geri çevir.
4.  Seçin **değişikliği isteği** onay kutusu kullanıcının belgede yapılan değişiklikleri isteyebilir.
5.  Seçin **temsilci** kullanıcı belgeyi onay için başka bir kullanıcıya atayabilirsiniz onay kutusunu.

**Not**: **Kurumsal Portal içindeki iş listesinden eylemleri etkinleştir ** onay kutusu kullanımdan kaldırılmıştır.

## <a name="configure-the-approval-steps"></a> Onay adımlarını yapılandırma
Onay işlemi onay adımlarından oluşur. Onay işlemine adım eklemek ve adımları yapılandırmak için aşağıdaki yordamı tamamlayın.
1.  İş akışı düzenleyicisinde onay işlemine çift tıklayın. İş akışı düzenleyicisi onay işleminin adımlarını görüntüler.
2.  Onay adımı eklemek için adımları **İş akışı öğeleri** alanından tuvale sürükleyin.
3.  Onay adımını yapılandırmak için bkz. [Onay adımını yapılandırma](http://axhelp.dynamics.com/en/wiki/configure-an-approval-step/).




