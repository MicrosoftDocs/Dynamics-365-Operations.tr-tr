---
title: "Bir iş akışında bir el ile kararı yapılandırma"
description: "Bu konu, el ile bir kararın özelliklerini yapılandırmayı açıklar."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ac86ffa794b5fd92ca9aba24537fbc05057fe824
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="configure-a-manual-decision-in-a-workflow"></a>Bir iş akışında bir el ile kararı yapılandırma

[!include[banner](../includes/banner.md)]


Bu konu, el ile bir kararın özelliklerini yapılandırmayı açıklar.

El ile bir kararı iş akışı düzenleyicisinde yapılandırmak için el ile karara sağ tıklatın ve sonra **Özellikler**'i açmak için **Özellikler** sayfanı tıklayın. Ardından el ile kararın özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.

## <a name="name-the-decision"></a>Kararın adı
El ile karara bir ad vermek için aşağıdaki adımları takip edin.

1.  Sol bölmede **Temel Ayarlar**'ı tıklatın.
2.  **Ad** alanına, el ile karar için benzersiz bir ad girin.

## <a name="enter-a-subject-line-and-instructions"></a>Konu satırı ve açıklamaları girme
Bu el ile karara atanmış olan kullanıcılara bir konu satırı ve açıklama sağlamanız gerekir. Örneğin, eğer satınalma talepleri için bir karar yapılandırıyorsanız, bu karara atanmış kullanıcı konu satırını ve yönergeleri **Satınalma talepleri** sayfasında görür. Konu satırı sayfa üzerindeki bir ileti çubuğunda görüntülenir. Daha sonra, kullanıcı yönergeleri görüntülemek için ileti çubuğundaki simgeye tıklayabilir. Konu satırını ve açıklamaları girmek için şu adımları kullanın.

1.  Sol bölmede **Temel Ayarlar**'ı tıklatın.
2.  **Yönergeler** sekmesinde, **Çalışma öğesi konusu** alanında, konu satırını girin.
3.  Konu satırını kişiselleştirmek için yer tutucular ekleyebilirsiniz. Yer tutucular, konu satırı kullanıcılara gösterildiğinde uygun verilerle değiştirilir. Yer tutucu eklemek için şu adımları izleyin:
    1.  Metin kutusunda, yer tutucunun görüneceği yere tıklayın.
    2.  **Yer tutucu ekle**'yi tıklatın.
    3.  Beliren listede, eklenecek yer tutucuyu seçin.
    4.  **Ekle**'yi tıklatın.

4.  Konu satırı çevirilerini eklemek için şu adımları izleyin:
    1.  **Çeviriler**'e tıklayın.
    2.  Beliren sayfada **Ekle**'yi tıklatın.
    3.  Beliren listede, metni girdiğiniz dili seçin.
    4.  **Çevrilen metin** alanında, metni girin.
    5.  Metni kişiselleştirmek için, 3. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.
    6.  **Kapat** düğmesini tıklayın.

5.  **Çalışma öğesi yönergeleri** alanında, yönergeleri girin.
6.  Yönergeleri kişiselleştirmek için, yer tutucular ekleyebilirsiniz. Yer tutucular, yönergeler kullanıcılara gösterildiğinde uygun verilerle değiştirilir. Yer tutucu eklemek için şu adımları izleyin:
    1.  Metin kutusunda, yer tutucunun görüneceği yere tıklayın.
    2.  **Yer tutucu ekle**'yi tıklatın.
    3.  Beliren listede, eklenecek yer tutucuyu seçin.
    4.  **Ekle**'yi tıklatın.

7.  Yönergelerin çevirilerini eklemek için şu adımları izleyin:
    1.  **Çeviriler**'e tıklayın.
    2.  Beliren sayfada **Ekle**'yi tıklatın.
    3.  Beliren listede, metni girdiğiniz dili seçin.
    4.  **Çevrilen metin** alanında, metni girin.
    5.  Metni kişiselleştirmek için, 6. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.
    6.  **Kapat** düğmesini tıklayın.

## <a name="specify-the-possible-outcomes-of-a-decision"></a>Bir kararın olası sonucunu belirtin
Genellikle bir belge bir karar vericiye atandığı zaman, karar vericiye bir soru sorulur. Sorunun yanıtı genellikle **Evet**veya **Hayır** ya da **Doğru** veya **Yanlış** olur. El ile kararın olası sonuçlarını belirtmek için aşağıdaki adımları izleyin.

1.  Sol bölmede **Temel Ayarlar**'ı tıklatın.
2.  **Sonuçlar** sekmesinde **Sonuç 1** alanında, sonucun adını veya seçeneği girin.
3.  Sonucun çevirilerini eklemek için şu adımları izleyin:
    1.  **Çeviriler**'e tıklayın.
    2.  Beliren sayfada **Ekle**'yi tıklatın.
    3.  Beliren listede, metni girdiğiniz dili seçin.
    4.  **Çevrilen metin** alanında, metni girin.
    5.  **Kapat** düğmesini tıklayın.

4.  **Sonuç 2** alanında, sonucun adını veya seçeneği girin.
5.  Sonucun çevirilerini eklemek için şu adımları izleyin:
    1.  **Çeviriler**'e tıklayın.
    2.  Beliren sayfada **Ekle**'yi tıklatın.
    3.  Beliren listede, metni girdiğiniz dili seçin.
    4.  **Çevrilen metin** alanında, metni girin.
    5.  **Kapat** düğmesini tıklayın.

## <a name="specify-when-notifications-are-sent"></a>Bildirimlerin ne zaman gönderileceğini belirtme
Bir karar alındığında, ilerletildiğinde veya yetkilendirildiğinde insanlara bildirim gönderebilirsiniz. Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.

1.  Sol bölmede **Bildirimler**'i tıklatın.
2.  Bildirimlerin gönderilmesi gerektiği etkinlikler için yanlarındaki onay kutusunu işaretleyin:
    -   **\[Seçim 1\]** – Atanan kullanıcı **\[Seçim 1\]**'i işaretledi.
    -   **\[Seçim 2\]** – Atanan kullanıcı **\[Seçim 2\]**'i işaretledi.
    -   **Temsilci** – Atanmış kullanıcı kararı başka bir kullanıcıya atadı.
    -   **İlerlet** – Atanmış kullanıcı, ayrılan sürede karar vermedi.

3.  2. adımda seçtiğiniz bir olay için bir satır seçin.
4.  **Bildirim metni** sekmesinde, metin kutusuna, bildirimin metnini girin.
5.  Bildirimi kişiselleştirmek için yer tutucular ekleyebilirsiniz. Yer tutucular, bildirim kullanıcılara gösterildiğinde uygun verilerle değiştirilir. Yer tutucu eklemek için şu adımları izleyin:
    1.  Metin kutusunda, yer tutucunun görüneceği yere tıklayın.
    2.  **Yer tutucu ekle**'yi tıklatın.
    3.  Beliren listede, eklenecek yer tutucuyu seçin.
    4.  **Ekle**'yi tıklatın.

6.  Bildirimin çevirilerini eklemek için şu adımları izleyin:
    1.  **Çeviriler**'e tıklayın.
    2.  Beliren sayfada **Ekle**'yi tıklatın.
    3.  Beliren listede, metni girdiğiniz dili seçin.
    4.  **Çevrilen metin** alanında, metni girin.
    5.  Metni kişiselleştirmek için, 5. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.
    6.  **Kapat** düğmesini tıklayın.

7.  **Alıcı** sekmesinde, bildirimlerin kime gönderildiğini belirtin. Aşağıdaki tablodaki seçeneklerden birini seçin ve 8. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.
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
    <td>Katılımcı</td>
    <td>Özel bir gruba ya da role atanmış kullanıcılar</td>
    <td><ol>
    <li><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, bildirimlerin gönderileceği grup ya da rolün türünü seçin.</li>
    <li><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>İş akışı kullanıcısı</td>
    <td>Mevcut iş akışındaki kullanıcılar</td>
    <td><ul>
    <li><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Kullanıcı</td>
    <td>Belirli Microsoft Dynamics 365 for Operations kullanıcıları</td>
    <td><ol>
    <li><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</li>
    <li><strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Dynamics 365 for Operations kullanıcılarını içerir. Bildirimlerin gönderileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.

## <a name="assign-a-decision"></a>Bir karar ata
El ile kararın kime atanacağını belirtmek için şu adımları izleyin.

1.  Sol bölmede **Atama**'yı tıklatın.
2.  **Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 3. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Seçenek</th>
    <th>Kararın atandığı kullanıcılar</th>
    <th>Ek adımlar</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Katılımcı</td>
    <td>Özel bir gruba ya da role atanmış kullanıcılar</td>
    <td><ol>
    <li><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, kararın atanacağı grup ya da rolün türünü seçin.</li>
    <li><strong>Katılımcı</strong> listesinde, kararın atanacağı grup veya rolü seçin.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hiyerarşi</td>
    <td>Belirli bir kuruluş hiyerarşisindeki kullanıcılar</td>
    <td><ol>
    <li><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, kararın atanacağı hiyerarşi türünü seçin.</li>
    <li>Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir. Bu adlar, kararın atanabileceği kullanıcıları temsil eder. Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin: <ol>
    <li>Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</li>
    <li>Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın. Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</li>
    </ol></li>
    <li><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara kararın atanması gerektiğini belirtin: <ul>
    <li><strong>Alınan tüm kullanıcılara ata</strong> – Karar, bu aralıktaki tüm kullanıcılara atanır.</li>
    <li><strong>Yalnızca alınan son kullanıcıya ata</strong> – Karar, yalnızca aralıktaki son kullanıcıya atanır.</li>
    <li><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Karar, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya atanmaz. Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>İş akışı kullanıcısı</td>
    <td>Mevcut iş akışındaki kullanıcılar</td>
    <td><ul>
    <li><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Kullanıcı</td>
    <td>Belirli Dynamics 365 for Operations kullanıcıları</td>
    <td><ol>
    <li><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</li>
    <li><strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Dynamics 365 for Operations kullanıcılarını içerir. Kararın atanacağı kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Kuyruk</td>
    <td>Bir iş maddesi kuyruğu</td>
    <td><ol>
    <li><strong>Kuyruk</strong>'u seçtikten sonra <strong>Kuyruk tabanlı</strong> sekmesini tıklatın.</li>
    <li>Kararı belirli bir kuyruğa atamak için şu adımları izleyin: <ol>
    <li><strong>Kuyruk türü</strong> listesinde, <strong>İş öğesi kuyrukları</strong>'nı seçin.</li>
    <li><strong>Kuyruk adı</strong> listesinde, kuyruğu seçin.</li>
    </ol></li>
    <li>Eğer belirli bir koşulun kararının hangi kuyruğa atanacağını belirlemesi gerekiyorsa, aşağıdaki adımları izleyin: <ol>
    <li><strong>Kuyruk türü</strong> listesinde, <strong>Koşullu iş öğesi kuyrukları</strong>'nı seçin.</li>
    <li><strong>Kuyruk adı</strong> listesinde, <strong>Koşullu kuyruk</strong>'u seçin.</li>
    </ol></li>
    </ol>
    <strong>Not:</strong> Bu seçenek yalnızca servis talebi yönetimi gibi bazı iş akışları için kullanılır.</td>
    </tr>
    </tbody>
    </table>

3.  **Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının kararı almak üzere ne kadar zamanı olduğunu belirtin. Aşağıdaki seçeneklerden birini belirleyin:
    -   **Saatler** – Kullanıcının kararı alması gereken saat sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    -   **Günler** – Kullanıcının kararı alması gereken gün sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    -   **Haftalar** – Kullanıcının kararı alması gereken hafta sayısını girin.
    -   **Aylar** – Kullanıcının kararı almış olması gereken günü ve haftayı seçin. Örneğin kullanıcının kararı ayın üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.
    -   **Yıllar** – Kullanıcının kararı almış olması gereken haftayı ve ayı seçin. Örneğin kullanıcının kararı Aralık ayının üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.

    Eğer kullanıcı ayırılan zaman içerisinde kararı alamazsa, kararın vadesi geçer. Vadesi geçmiş bir karar, sayfanın **İlerletme** bölgesinde işaretlemiş olduğunuz seçeneklere göre ilerletilir.

## <a name="specify-what-happens-when-a-decision-is-overdue"></a>Bir kararın süresi geçtiğinde ne olacağını belirtin
Eğer bir kullanıcı ayırılan zaman içerisinde kararı alamazsa, kararın vadesi geçer. Vadesi geçmiş bir karar ilerletilebilir veya başka bir kullanıcıya otomatik olarak atanabilir. Vadesi geçmiş ise, kararın üst düzeye ilerletilmesi için aşağıdaki adımları izleyin.

1.  Sol bölmede **İlerletilme**'yı tıklatın.
2.  İlerletme yolu oluşturmak için **İlerletme yolunu kullan** onay kutusunu seçin. Sistem kararı ilerletme yolunda listelenmiş olan kullanıcılara otomatik olarak atar. Örneğin, aşağıdaki tablo bir ilerletme yolunu temsil eder.
    | Seri | İlerletme yolu            |
    |----------|----------------------------|
    | 1        | Şu kişiye ata: Donna           |
    | 2        | Şu kişiye ata: Erin            |
    | 3        | Son eylem: \[Karar 1\] |

    Bu örnekte sistem süresi geçen kararı Donna'ya atar. Eğer Donna ayırılan süre içerisinde kararı alamazsa, sistem kararı Erin'e atar. Eğer Erin ayırılan süre içerisinde kararı alamazsa, sistem karar olarak **\[Karar 1\]**'i karar olarak seçer
3.  Bir kullanıcıyı ilerletme yoluna eklemek için **İlerletme ekle**'yi tıklatın. Aşağıdaki tablodaki seçeneklerden birini seçin ve 4. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Seçenek</th>
    <th>Kararın ilerletildiği kullanıcılar</th>
    <th>Ek adımlar</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Hiyerarşi</td>
    <td>Belirli bir kuruluş hiyerarşisindeki kullanıcılar</td>
    <td><ol>
    <li><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, kararın ilerletileceği hiyerarşi türünü seçin.</li>
    <li>Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir. Bu adlar kararın ilerletilebileceği kullanıcıları temsil eder. Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin: <ol>
    <li>Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</li>
    <li>Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın. Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</li>
    </ol></li>
    <li><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara kararın ilerletilmesi gerektiğini belirtin: <ul>
    <li><strong>Alınan tüm kullanıcılara ata</strong> – Karar bu aralıktaki tüm kullanıcılara ilerletilir.</li>
    <li><strong>Yalnızca alınan son kullanıcıya ata</strong> – Karar yalnızca aralıktaki son kullanıcıya ilerletilir.</li>
    <li><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak:</strong> – Karar, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya ilerletilmez. Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>İş akışı kullanıcısı</td>
    <td>Mevcut iş akışındaki kullanıcılar</td>
    <td><ul>
    <li><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Kullanıcı</td>
    <td>Belirli Dynamics 365 for Operations kullanıcıları</td>
    <td><ol>
    <li><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</li>
    <li><strong>Mevcut kullanıcılar</strong> listesi mevcut tüm Dynamics 365 for Operations kullanıcılarını içerir. Kararın ilerletileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  **Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının kararı almak üzere ne kadar zamanı olduğunu belirtin. Aşağıdaki seçeneklerden birini belirleyin:
    -   **Saatler** – Kullanıcının kararı alması gereken saat sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    -   **Günler** – Kullanıcının kararı alması gereken gün sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    -   **Haftalar** – Kullanıcının kararı alması gereken hafta sayısını girin.
    -   **Aylar** – Kullanıcının kararı almış olması gereken günü ve haftayı seçin. Örneğin kullanıcının kararı ayın üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.
    -   **Yıllar** – Kullanıcının kararı almış olması gereken haftayı ve ayı seçin. Örneğin kullanıcının kararı Aralık ayının üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.

5.  İlerletme yoluna eklenecek tüm kullanıcılar için 3. adım ve 4. adımlar arasındaki süreci yineleyin. Kullanıcıların sıralamasını değiştirebilirsiniz.
6.  İlerletme yolundaki kullanıcılar verilen süre içinde kararı alamazsa, sistem görev üstünde karar alır. Sistemin seçeceği seçeneği belirtmek için **Eylem** satırını seçin ve sonra **Eylemi bitir** sekmesi üzerinde bir seçenek seçin.

## <a name="set-a-time-limit"></a>Zaman limiti ayarlama
Kararın belirli bir süre içerisinde alınması gerekiyorsa bu adımları izleyin. **Not:** Bu yordamda belirlediğiniz seçenekler, sayfanın **Atama** ve **İlerletme** alanlarında belirlemiş olduğunuz seçenekleri geçersiz kılar.

1.  Sol bölmede **Gelişmiş ayarlar**'ı tıklatın.
2.  **İş akışı öğesi için bir zaman sınırı ayarlayın** onay kutusunu işaretleyin.
3.  **Süre** alanında, kararın ne zaman alınması gerektiğini belirtin. Aşağıdaki seçeneklerden birini belirleyin:
    -   **Saatler** – Saatlerin sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    -   **Günler** – Günlerin sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    -   **Haftalar** – Haftaların sayısını girin.
    -   **Aylar** – Kararın alınmış olması gereken günü ve haftayı seçin. Örneğin kararın ayın üçüncü haftasının Cuma gününden önce alınmış olmasını isteyebilirsiniz.
    -   **Yıllar** – Kararın alınmış olması gereken günü, haftayı ve ayı seçin. Örneğin kararın Aralık ayının üçüncü haftasının Cuma gününden önce alınmış olmasını isteyebilirsiniz.

4.  Zaman limiti aşılırsa sistem kararı kendi alır. **Eylem** listesinden sistemin tercih etmesi gereken seçeneği seçin.





