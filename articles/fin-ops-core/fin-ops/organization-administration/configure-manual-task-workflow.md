---
title: İş akışında el ile girilen görevleri yapılandırma
description: Bu konu, el ile bir görevin özelliklerini yapılandırmayı açıklar.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f61e0f7ee16519767192fb379f20c1ed20b69caa
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798817"
---
# <a name="configure-manual-tasks-in-a-workflow"></a>İş akışında el ile girilen görevleri yapılandırma

[!include [banner](../includes/banner.md)]

Bu konu, el ile bir görevin özelliklerini yapılandırmayı açıklar.

El ile bir görevi iş akışı düzenleyicisinde yapılandırmak için göreve sağ tıklatın ve sonra **Özellikler**'i açmak için **Özellikler** sayfanı tıklayın. Ardından el ile görevin özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.

## <a name="name-the-task"></a>Görevi adlandırma

El ile göreve bir ad vermek için aşağıdaki adımları takip edin.

1. Sol bölmede **Temel Ayarlar**'ı tıklatın.
2. **Ad** alanına görev için benzersiz bir ad girin.

## <a name="enter-a-subject-line-and-instructions"></a>Konu satırı ve açıklamaları girme

Göreve atanan kullanıcılara bir konu satırı ve açıklama sağlamanız gerekir. Örneğin, eğer satınalma talepleri için bir görev yapılandırıyorsanız, bu göreve atanmış kullanıcı konu satırını ve yönergeleri **Satınalma talepleri** sayfasında görür. Konu satırı sayfa üzerindeki bir ileti çubuğunda görüntülenir. Daha sonra, kullanıcı yönergeleri görüntülemek için ileti çubuğundaki simgeye tıklayabilir. Konu satırını ve açıklamaları girmek için şu adımları kullanın.

1. Sol bölmede **Temel Ayarlar**'ı tıklatın.
2. **Çalışma öğesi konusu** alanında, konu satırını girin.
3. Konu satırını kişiselleştirmek için yer tutucular ekleyebilirsiniz. Yer tutucular, konu satırı kullanıcılara gösterildiğinde uygun verilerle değiştirilir. Yer tutucu eklemek için şu adımları izleyin:

    1. Metin kutusunda, yer tutucunun görüneceği yere tıklayın.
    2. **Yer tutucu ekle**'yi tıklatın.
    3. Beliren listede, eklenecek yer tutucuyu seçin.
    4. **Ekle**'yi tıklatın.

4. Konu satırı çevirilerini eklemek için şu adımları izleyin:

    1. **Çeviriler**'e tıklayın.
    2. Beliren sayfada **Ekle**'yi tıklatın.
    3. Beliren listede, metni girdiğiniz dili seçin.
    4. **Çevrilen metin** alanında, metni girin.
    5. Metni kişiselleştirmek için, 3. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.
    6. **Kapat** düğmesini tıklayın.

5. **Çalışma öğesi yönergeleri** alanında, yönergeleri girin.
6. Yönergeleri kişiselleştirmek için, yer tutucular ekleyebilirsiniz. Yer tutucular, yönergeler kullanıcılara gösterildiğinde uygun verilerle değiştirilir. Yer tutucu eklemek için şu adımları izleyin:

    1. Metin kutusunda, yer tutucunun görüneceği yere tıklayın.
    2. **Yer tutucu ekle**'yi tıklatın.
    3. Beliren listede, eklenecek yer tutucuyu seçin.
    4. **Ekle**'yi tıklatın.

7. Yönergelerin çevirilerini eklemek için şu adımları izleyin:

    1. **Çeviriler**'e tıklayın.
    2. Beliren sayfada **Ekle**'yi tıklatın.
    3. Beliren listede, metni girdiğiniz dili seçin.
    4. **Çevrilen metin** alanında, metni girin.
    5. Metni kişiselleştirmek için, 6. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.
    6. **Kapat** düğmesini tıklayın.

## <a name="assign-the-task"></a>Görev atama

El ile görev kime atanacağını belirtmek için şu adımları izleyin:

1. Sol bölmede **Atama**'yı tıklatın.
2. **Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 3. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.

    <table>
    <thead>
    <tr>
    <th>Seçenek</th>
    <th>Görevin atandığı kullanıcılar</th>
    <th>Ek adımlar</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Katılımcı</td>
    <td>Özel bir gruba ya da role atanmış kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, görevin atanacağı grup ya da rolün türünü seçin.</li>
    <li><strong>Katılımcı</strong> listesinde, görevin atanacağı grup veya rolü seçin.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hiyerarşi</td>
    <td>Belirli bir kuruluş hiyerarşisindeki kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, görevin atanacağı hiyerarşi türünü seçin.</li>
    <li>Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir. Bu adlar, görevin atanabileceği kullanıcıları temsil eder. Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin: <ol>
    <li>Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</li>
    <li>Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın. Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</li>
    </ol>
    </li>
    <li><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara görevin atanması gerektiğini belirtin: <ul>
    <li><strong>Alınan tüm kullanıcılara ata</strong> – Görev, bu aralıktaki tüm kullanıcılara atanır.</li>
    <li><strong>Yalnızca alınan son kullanıcıya ata</strong> – Görev, yalnızca aralıktaki son kullanıcıya atanır.</li>
    <li><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Görev, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya atanmaz. Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>İş akışı kullanıcısı</td>
    <td>Mevcut iş akışındaki kullanıcılar</td>
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
    <li><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm  kullanıcılarını içerir. Görevin atanacağı kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Kuyruk</td>
    <td>Bir iş maddesi kuyruğu</td>
    <td>
    <ol>
    <li><strong>Kuyruk</strong>'u seçtikten sonra <strong>Kuyruk tabanlı</strong> sekmesini tıklatın.</li>
    <li>Görevi belirli bir kuyruğa atamak için şu adımları izleyin: <ol>
    <li><strong>Kuyruk türü</strong> listesinde, <strong>İş öğesi kuyrukları</strong>'nı seçin.</li>
    <li><strong>Kuyruk adı</strong> listesinde, kuyruğu seçin.</li>
    </ol>
    </li>
    <li>Eğer belirli bir koşulun görevin hangi kuyruğa atanacağını belirlemesi gerekiyorsa, aşağıdaki adımları izleyin: <ol>
    <li><strong>Kuyruk türü</strong> listesinde, <strong>Koşullu iş öğesi kuyrukları</strong>'nı seçin.</li>
    <li><strong>Kuyruk adı</strong> listesinde, <strong>Koşullu kuyruk</strong>'u seçin.</li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] Bu seçenek yalnızca servis talebi yönetimi gibi bazı iş akışları için kullanılır.</blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. **Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının görevi tamamlamak üzere ne kadar zamanı olduğunu belirtin. Aşağıdaki seçeneklerden birini belirleyin:

    - **Saatler** – Kullanıcının görevi tamamlaması gereken saat sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Günler** – Kullanıcının görevi tamamlaması gereken gün sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Haftalar** – Kullanıcının görevi tamamlaması gereken hafta sayısını girin.
    - **Aylar** – Kullanıcının görevi tamamlamış olması gereken günü ve haftayı seçin. Örneğin kullanıcının görevi ayın üçüncü haftasının Cuma günü tamamlamasını isteyebilirsiniz.
    - **Yıllar** – Kullanıcının görevi tamamlamış olması gereken günü, haftayı ve ayı seçin. Örneğin kullanıcının görevi Aralık ayının üçüncü haftasının Cuma günü tamamlamasını isteyebilirsiniz.

    Eğer kullanıcı ayırılan zaman içerisinde görevi tamamlamazsa, görevin vadesi geçer. Vadesi geçmiş bir görev, sayfanın **İlerletme** bölgesinde işaretlemiş olduğunuz seçeneklere göre ilerletilebilir.

## <a name="specify-what-happens-when-the-task-is-overdue"></a>Görevin süresi geçtiğinde ne olacağını belirtin

Eğer bir kullanıcı ayırılan zaman içerisinde el ile görevi tamamlamazsa, görevin vadesi geçer. Vadesi geçmiş bir görev ilerletilebilir veya başka bir kullanıcıya otomatik olarak atanabilir. Vadesi geçmiş ise, görevin üst düzeye ilerletilmesi için aşağıdaki adımları izleyin.

1. Sol bölmede **İlerletilme**'yı tıklatın.
2. İlerletme yolu oluşturmak için **İlerletme yolunu kullan** onay kutusunu seçin. Sistem görevi ilerletme yolunda listelenmiş olan kullanıcılara otomatik olarak atar. Örneğin, aşağıdaki tablo bir ilerletme yolunu temsil eder.

    | Seri | İlerletme yolu      |
    |----------|----------------------|
    | 1        | Şu kişiye ata: Donna     |
    | 2        | Şu kişiye ata: Erin      |
    | 3        | Son eylem: Reddet |

    Bu örnekte sistem süresi geçen görevi Donna'ya atar. Eğer Donna ayırılan süre içerisinde görevi tamamlamazsa, sistem görevi Erin'e atar. Eğer Erin ayırılan süre içerisinde görevi tamamlamazsa, sistem işlenmek üzere gönderilen belgeyi reddeder.

3. Bir kullanıcıyı ilerletme yoluna eklemek için **İlerletme ekle**'yi tıklatın. **Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 4. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.

    <table>
    <thead>
    <tr>
    <th>Seçenek</th>
    <th>Görevin ilerletileceği kullanıcılar</th>
    <th>Ek adımlar</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hiyerarşi</td>
    <td>Belirli bir kuruluş hiyerarşisindeki kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, görevin ilerletileceği hiyerarşi türünü seçin.</li>
    <li>Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir. Bu adlar, görevin ilerletilebileceği kullanıcıları temsil eder. Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin: <ol>
    <li>Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</li>
    <li>Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın. Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</li>
    </ol>
    </li>
    <li><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara görevin ilerletilmesi gerektiğini belirtin: <ul>
    <li><strong>Alınan tüm kullanıcılara ata</strong> – Görev, bu aralıktaki tüm kullanıcılara ilerletilir.</li>
    <li><strong>Yalnızca alınan son kullanıcıya ata</strong> – Görev, yalnızca aralıktaki son kullanıcıya ilerletilir.</li>
    <li><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Bu görev, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya ilerletilmez. Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>İş akışı kullanıcısı</td>
    <td>Mevcut iş akışındaki kullanıcılar</td>
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
    <li><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm  kullanıcılarını içerir. Görevin ilerletileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. **Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının görevi tamamlamak üzere ne kadar zamanı olduğunu belirtin. Aşağıdaki seçeneklerden birini belirleyin:

    - **Saatler** – Kullanıcının görevi tamamlaması gereken saat sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Günler** – Kullanıcının görevi tamamlaması gereken gün sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Haftalar** – Kullanıcının görevi tamamlaması gereken hafta sayısını girin.
    - **Aylar** – Kullanıcının görevi tamamlamış olması gereken günü ve haftayı seçin. Örneğin kullanıcının görevi ayın üçüncü haftasının Cuma günü tamamlamasını isteyebilirsiniz.
    - **Yıllar** – Kullanıcının görevi tamamlamış olması gereken günü, haftayı ve ayı seçin. Örneğin kullanıcının görevi Aralık ayının üçüncü haftasının Cuma günü tamamlamasını isteyebilirsiniz.

5. İlerletme yoluna eklenecek tüm kullanıcılar için 3. adım ve 4. adımlar arasındaki süreci yineleyin. Kullanıcıların sıralamasını değiştirebilirsiniz.
6. İlerletme yolundaki kullanıcılar verilen süre içinde görevi tamamlamazsa, sistem görev üstünde otomatik olarak eylem alır. Sistemin alacağı eylemi belirtmek için **Eylem** satırını seçin ve sonra **Eylemi bitir** sekmesi üzerinde bir eylem seçin.

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a>Sistemin ne zaman görev üzerinde otomatik olarak eylem alacağını belirtin

Belirli koşullar sağlandığında sistemin el ile görevler üzerinde eylem almasını yapılandırabilirsiniz. Örneğin, bir görev, Gider raporları departmanının bir üyesinin, bir gider raporu ile birlikte gönderilen girişleri gözden geçirmesini gerektirmektedir. Şirket ilkesi uyarınca, bu görev, gider raporunun toplam tutarı 100 USD'den fazlaysa gerçekleştirilmek zorundadır. Bu senaryoda, toplam tutar 100'den az ise sistemi, görevi otomatik olarak **Tamamlandı** olarak işaretlemek üzere yapılandırabilirsiniz. Sistemin bir el ile görev üzerinde ne zaman eylem alması gerektiğin belirtmek için aşağıdaki adımları izleyin:

1. Sol bölmede **Otomatik eylemler**'ı tıklatın.
2. **Otomatik eylemleri etkinleştir** onay kutusunu işaretleyin.
3. **Koşul ekle** seçeneğini tıklatın.
4. Koşulu girin.
5. Varsa, gerekli ek koşulları girin.
6. Girdiğiniz koşulların doğru biçimde yapılandırıldığını doğrulamak için, aşağıdaki adımları izleyin:

    1. **Sına**'yı tıklatın.
    2. **İş akışını test et** sayfasında, **Koşulu doğrula** alanında, bir kayıt seçin.
    3. **Sına**'yı tıklatın. Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.
    4. **Özellikler** sayfasında geri dönmek için **OK** ya da **İptal Et**'e tıklayın.

7. **Eylemi otomatik tamamla** listesinden sistemin görev üzerinde gerçekleştirmesi gereken eylemi seçin.

## <a name="specify-when-notifications-are-sent"></a>Bildirimlerin ne zaman gönderileceğini belirtme

Bir el ile görev tamamlandığında, temsilci atandığında, ilerletildiğinde, tamamlandığında, reddedildiğinde veya bir değişiklik istendiğinde kişilere bildirim gönderebilirsiniz. Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.

1. Sol bölmede **Bildirimler**'i tıklatın.
2. Bildirimlerin gönderilmesi gerektiği etkinlikler için yanlarındaki onay kutusunu işaretleyin:

    - **Temsilci** – Görev başka bir kullanıcıya atandı.
    - **İlerlet** – Atanmış kullanıcı, ayrılan sürede görevi tamamlamadı.
    - **Tamamlandı** – Atanmış kullanıcı, görevi tamamlandı.
    - **Reddetme** – Atanmış kullanıcı gönderilen belgeyi reddetti.
    - **Değişiklik iste** – Atanmış kullanıcı gönderilmiş olan belgede bir değişiklik talep etti.

3. 2. adımda seçtiğiniz bir olay için bir satır seçin.
4. **Bildirim metni** sekmesinde, metin kutusuna, bildirimin metnini girin.
5. Bildirimi kişiselleştirmek için yer tutucular ekleyebilirsiniz. Yer tutucular, bildirim kullanıcılara gösterildiğinde uygun bilgilerle değiştirilir. Yer tutucu eklemek için şu adımları izleyin:

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
    <td>Mevcut iş akışındaki kullanıcılar</td>
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

## <a name="set-a-time-limit"></a>Zaman limiti ayarlama

El ile görevin belirli bir süre içerisinde tamamlanması gerekiyorsa bu adımları izleyin.

> [!NOTE]
> Bu yordamda belirlediğiniz seçenekler, sayfanın **Atama** ve **İlerletme** alanlarında belirlemiş olduğunuz seçenekleri geçersiz kılar.

1. Sol bölmede **Gelişmiş ayarlar**'ı tıklatın.
2. **İş akışı öğesi için bir zaman sınırı ayarlayın** onay kutusunu işaretleyin.
3. **Süre** alanında, görevin ne zaman tamamlanması gerektiğini belirtin. Aşağıdaki seçeneklerden birini belirleyin:

    - **Saatler** – Görevin tamamlaması gereken saat sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Günler** – Görevin tamamlaması gereken gün sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Haftalar** – Görevin tamamlaması gereken hafta sayısını girin.
    - **Aylar** – Görevin tamamlamış olması gereken günü ve haftayı seçin. Örneğin görevin ayın üçüncü haftasının Cuma gününden önce tamamlanmış olmasını isteyebilirsiniz.
    - **Yıllar** – Görevin tamamlamış olması gereken günü, haftayı ve ayı seçin. Örneğin görevin Aralık ayının üçüncü haftasının Cuma gününden önce tamamlanmış olmasını isteyebilirsiniz.

4. Zaman limiti aşılırsa sistem görev üstünde eylem yapar. **Eylem** listesinde sistemin gerçekleştirmesi gereken eylemi seçin.

## <a name="specify-which-actions-are-available-to-the-user"></a>Hangi eylemlerin kullanıcı tarafından kullanılabilir olacağını belirtin

El ile görev bir kullanıcıya atandığında kullanıcı görev üstünde eylem yapmalıdır. Kullanıcının görev üzerinde hangi eylemleri yapabileceğini belirtmek için bu adımları izleyin:

> [!NOTE]
> Gerçekleştirilebilecek eylemler, görevin tasarımına bağlı olarak değişebilir.

1. Sol bölmede **Gelişmiş ayarlar**'ı tıklatın.
2. Eğer kullanıcı görevi **Tamamlanmış** olarak işaretleyebilecekse, **Tamamlandı** onay kutusunu işaretleyin.
3. Eğer kullanıcı gönderilen belgeyi reddedebilecekse, **Reddet** onay kutusunu işaretleyin.
4. Kullanıcı gönderilen belgede değişiklik talep edebilecekse **Değişiklik iste** onay kutusunu seçin.
5. Kullanıcı görevi başka bir kullanıcıya atayabilecekse **Temsilci seç** onay kutusunu işaretleyin.
6. Kullanıcı görevi, iş öğesi kuyruğundaki başka bir kullanıcıya yeniden atayabilecekse **Yeniden Ata** onay kutusunu işaretleyin.
7. Kullanıcı görevi, iş öğesi kuyruğundaki başka bir kullanıcıya serbest bırakabilecekse, **Serbest Bırak** onay kutusunu işaretleyin. Daha sonra başka bir kullanıcı bu görevi tamamlayabilir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]