---
title: İş akışında el ile girilen kararları yapılandırma
description: Bu makalede, el ile girilen bir kararın özelliklerinin nasıl yapılandırılacağı açıklanmaktadır.
author: ChrisGarty
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c143da04c5398190f1f5e4d2ec9eb07c6421459f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910301"
---
# <a name="configure-manual-decisions-in-a-workflow"></a>İş akışında el ile girilen kararları yapılandırma

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Bu makalede, el ile girilen bir kararın özelliklerinin nasıl yapılandırılacağı açıklanmaktadır.

El ile bir kararı iş akışı düzenleyicisinde yapılandırmak için el ile karara sağ tıklatın ve sonra **Özellikler**'i açmak için **Özellikler** sayfanı tıklayın. Ardından el ile kararın özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.

## <a name="name-the-decision"></a>Kararın adı

El ile karara bir ad vermek için aşağıdaki adımları takip edin.

1. Sol bölmede **Temel Ayarlar**'ı tıklatın.
2. **Ad** alanına, el ile karar için benzersiz bir ad girin.

## <a name="enter-a-subject-line-and-instructions"></a>Konu satırı ve açıklamaları girme

Bu el ile karara atanmış olan kullanıcılara bir konu satırı ve açıklama sağlamanız gerekir. Örneğin, eğer satınalma talepleri için bir karar yapılandırıyorsanız, bu karara atanmış kullanıcı konu satırını ve yönergeleri **Satınalma talepleri** sayfasında görür. Konu satırı sayfa üzerindeki bir ileti çubuğunda görüntülenir. Daha sonra, kullanıcı yönergeleri görüntülemek için ileti çubuğundaki simgeye tıklayabilir. Konu satırını ve açıklamaları girmek için şu adımları kullanın.

1. Sol bölmede **Temel Ayarlar**'ı tıklatın.
2. **Yönergeler** sekmesinde, **Çalışma öğesi konusu** alanında, konu satırını girin.
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

## <a name="specify-the-possible-outcomes-of-a-decision"></a>Bir kararın olası sonucunu belirtin

Genellikle bir belge bir karar vericiye atandığı zaman, karar vericiye bir soru sorulur. Sorunun yanıtı genellikle **Evet** veya **Hayır** ya da **Doğru** veya **Yanlış** olur. El ile kararın olası sonuçlarını belirtmek için aşağıdaki adımları izleyin.

1. Sol bölmede **Temel Ayarlar**'ı tıklatın.
2. **Sonuçlar** sekmesinde **Sonuç 1** alanında, sonucun adını veya seçeneği girin.
3. Sonucun çevirilerini eklemek için şu adımları izleyin:

    1. **Çeviriler**'e tıklayın.
    2. Beliren sayfada **Ekle**'yi tıklatın.
    3. Beliren listede, metni girdiğiniz dili seçin.
    4. **Çevrilen metin** alanında, metni girin.
    5. **Kapat** düğmesini tıklayın.

4. **Sonuç 2** alanında, sonucun adını veya seçeneği girin.
5. Sonucun çevirilerini eklemek için şu adımları izleyin:

    1. **Çeviriler**'e tıklayın.
    2. Beliren sayfada **Ekle**'yi tıklatın.
    3. Beliren listede, metni girdiğiniz dili seçin.
    4. **Çevrilen metin** alanında, metni girin.
    5. **Kapat** düğmesini tıklayın.

## <a name="specify-when-notifications-are-sent"></a>Bildirimlerin ne zaman gönderileceğini belirtme

Bir karar alındığında, ilerletildiğinde veya yetkilendirildiğinde insanlara bildirim gönderebilirsiniz. Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.

1. Sol bölmede **Bildirimler**'i tıklatın.
2. Bildirimlerin gönderilmesi gerektiği etkinlikler için yanlarındaki onay kutusunu işaretleyin:

    - **\[Seçim 1\]** – Atanan kullanıcı **\[Seçim 1\]**'i işaretledi.
    - **\[Seçim 2\]** – Atanan kullanıcı **\[Seçim 2\]**'i işaretledi.
    - **Temsilci** – Atanmış kullanıcı kararı başka bir kullanıcıya atadı.
    - **İlerlet** – Atanmış kullanıcı, ayrılan sürede karar vermedi.

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

## <a name="assign-a-decision"></a>Bir karar ata

El ile kararın kime atanacağını belirtmek için şu adımları izleyin.

1. Sol bölmede **Atama**'yı tıklatın.
2. **Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 3. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.

    <table>
    <thead>
    <tr>
    <th>Seçenek</th>
    <th>Kararın atandığı kullanıcılar</th>
    <th>Ek adımlar</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Katılımcı</td>
    <td>Özel bir gruba ya da role atanmış kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, kararın atanacağı grup ya da rolün türünü seçin.</li>
    <li><strong>Katılımcı</strong> listesinde, kararın atanacağı grup veya rolü seçin.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hiyerarşi</td>
    <td>Belirli bir kuruluş hiyerarşisindeki kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, kararın atanacağı hiyerarşi türünü seçin.</li>
    <li>Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir. Bu adlar, kararın atanabileceği kullanıcıları temsil eder. Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin: <ol>
    <li>Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</li>
    <li>Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın. Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</li>
    </ol>
    </li>
    <li><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara kararın atanması gerektiğini belirtin: <ul>
    <li><strong>Alınan tüm kullanıcılara ata</strong> – Karar, bu aralıktaki tüm kullanıcılara atanır.</li>
    <li><strong>Yalnızca alınan son kullanıcıya ata</strong> – Karar, yalnızca aralıktaki son kullanıcıya atanır.</li>
    <li><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Karar, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya atanmaz. Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</li>
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
    <li><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm  kullanıcılarını içerir. Kararın atanacağı kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. **Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının kararı almak üzere ne kadar zamanı olduğunu belirtin. Aşağıdaki seçeneklerden birini belirleyin:

    - **Saatler** – Kullanıcının kararı alması gereken saat sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Günler** – Kullanıcının kararı alması gereken gün sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Haftalar** – Kullanıcının kararı alması gereken hafta sayısını girin.
    - **Aylar** – Kullanıcının kararı almış olması gereken günü ve haftayı seçin. Örneğin kullanıcının kararı ayın üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.
    - **Yıllar** – Kullanıcının kararı almış olması gereken haftayı ve ayı seçin. Örneğin kullanıcının kararı Aralık ayının üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.

    Eğer kullanıcı ayırılan zaman içerisinde kararı alamazsa, kararın vadesi geçer. Vadesi geçmiş bir karar, sayfanın **İlerletme** bölgesinde işaretlemiş olduğunuz seçeneklere göre ilerletilir.

## <a name="specify-what-happens-when-a-decision-is-overdue"></a>Bir kararın süresi geçtiğinde ne olacağını belirtin

Eğer bir kullanıcı ayırılan zaman içerisinde kararı alamazsa, kararın vadesi geçer. Vadesi geçmiş bir karar ilerletilebilir veya başka bir kullanıcıya otomatik olarak atanabilir. Vadesi geçmiş ise, kararın üst düzeye ilerletilmesi için aşağıdaki adımları izleyin.

1. Sol bölmede **İlerletilme**'yı tıklatın.
2. İlerletme yolu oluşturmak için **İlerletme yolunu kullan** onay kutusunu seçin. Sistem kararı ilerletme yolunda listelenmiş olan kullanıcılara otomatik olarak atar. Örneğin, aşağıdaki tablo bir ilerletme yolunu temsil eder.

    | Seri | İlerletme yolu            |
    |----------|----------------------------|
    | 1        | Şu kişiye ata: Donna           |
    | 2        | Şu kişiye ata: Erin            |
    | 3        | Son eylem: \[Karar 1\] |

    Bu örnekte sistem süresi geçen kararı Donna'ya atar. Eğer Donna ayırılan süre içerisinde kararı alamazsa, sistem kararı Erin'e atar. Eğer Erin ayırılan süre içerisinde kararı alamazsa, sistem karar olarak **\[Karar 1\]**'i karar olarak seçer

3. Bir kullanıcıyı ilerletme yoluna eklemek için **İlerletme ekle**'yi tıklatın. Aşağıdaki tablodaki seçeneklerden birini seçin ve 4. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.

    <table>
    <thead>
    <tr>
    <th>Seçenek</th>
    <th>Kararın ilerletildiği kullanıcılar</th>
    <th>Ek adımlar</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hiyerarşi</td>
    <td>Belirli bir kuruluş hiyerarşisindeki kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, kararın ilerletileceği hiyerarşi türünü seçin.</li>
    <li>Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir. Bu adlar kararın ilerletilebileceği kullanıcıları temsil eder. Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin: <ol>
    <li>Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</li>
    <li>Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın. Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</li>
    </ol>
    </li>
    <li><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara kararın ilerletilmesi gerektiğini belirtin: <ul>
    <li><strong>Alınan tüm kullanıcılara ata</strong> – Karar bu aralıktaki tüm kullanıcılara ilerletilir.</li>
    <li><strong>Yalnızca alınan son kullanıcıya ata</strong> – Karar yalnızca aralıktaki son kullanıcıya ilerletilir.</li>
    <li><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak:</strong> – Karar, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya ilerletilmez. Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</li>
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
    <li><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm  kullanıcılarını içerir. Kararın ilerletileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. **Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının kararı almak üzere ne kadar zamanı olduğunu belirtin. Aşağıdaki seçeneklerden birini belirleyin:

    - **Saatler** – Kullanıcının kararı alması gereken saat sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Günler** – Kullanıcının kararı alması gereken gün sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Haftalar** – Kullanıcının kararı alması gereken hafta sayısını girin.
    - **Aylar** – Kullanıcının kararı almış olması gereken günü ve haftayı seçin. Örneğin kullanıcının kararı ayın üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.
    - **Yıllar** – Kullanıcının kararı almış olması gereken haftayı ve ayı seçin. Örneğin kullanıcının kararı Aralık ayının üçüncü haftasının Cuma gününe kadar almasını isteyebilirsiniz.

5. İlerletme yoluna eklenecek tüm kullanıcılar için 3. adım ve 4. adımlar arasındaki süreci yineleyin. Kullanıcıların sıralamasını değiştirebilirsiniz.
6. İlerletme yolundaki kullanıcılar verilen süre içinde kararı alamazsa, sistem görev üstünde karar alır. Sistemin seçeceği seçeneği belirtmek için **Eylem** satırını seçin ve sonra **Eylemi bitir** sekmesi üzerinde bir seçenek seçin.

## <a name="set-a-time-limit"></a>Zaman limiti ayarlama

Kararın belirli bir süre içerisinde alınması gerekiyorsa bu adımları izleyin.

> [!NOTE]
> Bu yordamda belirlediğiniz seçenekler, sayfanın **Atama** ve **İlerletme** alanlarında belirlemiş olduğunuz seçenekleri geçersiz kılar.

1. Sol bölmede **Gelişmiş ayarlar**'ı tıklatın.
2. **İş akışı öğesi için bir zaman sınırı ayarlayın** onay kutusunu işaretleyin.
3. **Süre** alanında, kararın ne zaman alınması gerektiğini belirtin. Aşağıdaki seçeneklerden birini belirleyin:

    - **Saatler** – Saatlerin sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Günler** – Günlerin sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Haftalar** – Haftaların sayısını girin.
    - **Aylar** – Kararın alınmış olması gereken günü ve haftayı seçin. Örneğin kararın ayın üçüncü haftasının Cuma gününden önce alınmış olmasını isteyebilirsiniz.
    - **Yıllar** – Kararın alınmış olması gereken günü, haftayı ve ayı seçin. Örneğin kararın Aralık ayının üçüncü haftasının Cuma gününden önce alınmış olmasını isteyebilirsiniz.

4. Zaman limiti aşılırsa sistem kararı kendi alır. **Eylem** listesinden sistemin tercih etmesi gereken seçeneği seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]