---
title: İş akışında onay adımlarını yapılandırma
description: Bu konu, bir onay adımının özelliklerini yapılandırmayı açıklar.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84ff82dcb9f4ce930b4f1122790f7989c56fac35
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070789"
---
# <a name="configure-approval-steps-in-a-workflow"></a>İş akışında onay adımlarını yapılandırma

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Bu konu, bir onay adımının özelliklerini yapılandırmayı açıklar.

Bir onay adımını iş akışı düzenleyicisinde yapılandırmak için onay adımına sağ tıklatın ve sonra **Özellikler**'i açmak için **Özellikler** sayfanı tıklayın. Ardından onay adımının özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.

## <a name="name-the-step"></a>Adımı adlandırma
Onay adımına bir ad vermek için aşağıdaki adımları takip edin.

1. Sol bölmede **Temel Ayarlar**'ı tıklatın.
2. **Ad** alanına onay adımı için benzersiz bir ad girin.

## <a name="enter-a-subject-line-and-instructions"></a>Konu satırı ve açıklamaları girme

Bu onay adımına atanmış olan kullanıcılara bir konu satırı ve açıklama sağlamanız gerekir. Örneğin, eğer satınalma talepleri için bir onay adımı yapılandırıyorsanız, bu adıma atanmış kullanıcı konu satırını ve yönergeleri **Satınalma talepleri** sayfasında görür. Konu satırı sayfa üzerindeki bir ileti çubuğunda görüntülenir. Daha sonra, kullanıcı yönergeleri görmek için ileti çubuğundaki simgeye tıklayabilir. Konu satırını ve açıklamaları girmek için şu adımları kullanın.

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

## <a name="assign-the-approval-step"></a>Onay adımını atama

Onay adımının kime atanacağını belirtmek için şu adımları izleyin:

1. Sol bölmede **Atama**'yı tıklatın.
2. **Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 3. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.

    <table>
    <thead>
    <tr>
    <th>Seçenek</th>
    <th>Onay adımının atandığı kullanıcılar</th>
    <th>Ek adımlar</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Katılımcı</td>
    <td>Özel bir gruba ya da role atanmış kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, adımın atanacağı grup ya da rolün türünü seçin.</li>
    <li><strong>Katılımcı</strong> listesinde, adımın atanacağı grup veya rolü seçin.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hiyerarşi</td>
    <td>Belirli bir kuruluş hiyerarşisindeki kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, adımın atanacağı hiyerarşi türünü seçin.</li>
    <li>Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir. Bu adlar, adımın atanabileceği kullanıcıları temsil eder. Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin: <ol>
    <li>Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</li>
    <li>Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın. Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</li>
    </ol>
    </li>
    <li><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara adımın atanması gerektiğini belirtin: <ul>
    <li><strong>Alınan tüm kullanıcılara ata</strong> – Adım, bu aralıktaki tüm kullanıcılara atanır.</li>
    <li><strong>Yalnızca alınan son kullanıcıya ata</strong> – Adım, yalnızca aralıktaki son kullanıcıya atanır.</li>
    <li><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Adım, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya atanmaz. Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</li>
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
    <li><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm sistem kullanıcılarını içerir. Adımların atanacağı kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. **Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının onay adımına ulaşan belgelere yanıt vermek veya bunlar üzerinde eyleme geçmek üzere ne kadar zamanı olduğunu belirtin. Aşağıdaki seçeneklerden birini belirleyin:

    - **Saatler** – Kullanıcının yanıt vermesi gereken saat sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Günler** – Kullanıcının yanıt vermesi gereken gün sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Haftalar** – Kullanıcının yanıt vermesi gereken hafta sayısını girin.
    - **Aylar** – Kullanıcının yanıt vermesi gereken günü ve haftayı seçin. Örneğin, kullanıcının ayın üçüncü haftasındaki Cuma günü yanıt vermesini isteyebilirsiniz.
    - **Yıllar** – Kullanıcının yanıt vermesi gereken haftayı ve ayı seçin. Örneğin, kullanıcının Aralık ayının üçüncü haftasındaki Cuma günü yanıt vermesini isteyebilirsiniz.

    Eğer kullanıcı bu zaman içerisinde belge üzerinde eyleme geçmezse, belgenin vadesi geçer. Vadesi geçmiş bir belge, sayfanın **İlerletme** bölgesinde işaretlemiş olduğunuz seçeneklere göre ilerletilir.

4. Eğer onay adımını birden fazla kullanıcıya ya da bir kullanıcı grubuna atadıysanız, **Tamamlanma ilkesi** sekmesinde aşağıdaki seçeneklerden birini işaretleyin:

    - **Tek onaylayan** – Belgeye uygulanan eylem, yanıt veren ilk kişi tarafından belirlenir. Örneğin, Sam 15.000 USD tutarında bir gider raporu gönderdi. Gider raporu şu an Sue, Jo ve Bill'e atanmıştır. Eğer Sue belgeye ilk yanıt veren kişi olursa, onun aldığı eylem belgeye uygulanır. Sue belgeyi reddederse, belge reddedilir ve Sam'e geri gönderilir. Sue belgeyi onaylarsa, onaylanmak üzere Ann'e gönderilir.

        ![Onay işlemine sahip bir iş akışı.](./media/workflow_multipleusersinstep.gif)

    - **Onaylayanların çoğunluğu** – Belgeye uygulanan eylem, onaylayanların çoğunluğu yanıt verdiğinde belirlenir. Örneğin, Sam 15.000 USD tutarında bir gider raporu gönderdi. Gider raporu şu an Sue, Jo ve Bill'e atanmıştır. Eğer Sue ve Jo yanıt veren ilk iki kişiyse, aldıkları eylem belgeye uygulanır.

        - Sue belgeyi onaylar ama Jo reddederse, belge reddedilir ve Sam'e geri gönderilir.
        - Eğer hem Sue hem de Jo belgeye onay verirse, onay için Ann'e gönderilir.

    - **Onaylayanların yüzdesi** – Belgeye uygulanan eylem, onaylayanların belirli bir yüzdesi yanıt verdiğinde belirlenir. Örneğin, Sam 15.000 USD tutarında bir gider raporu gönderdi. Gider raporu şu anda Sue, Jo ve Bill'e atanmıştır ve oran olarak **50** girdiniz. Eğer Sue ve Jo yanıt veren ilk iki kişi olurlarsa, onların aldıkları eylem belgeye uygulanır çünkü onaylayanların yüzde 50'si gereksinimini karşılamaktadırlar.

        - Sue belgeyi onaylar ama Jo reddederse, belge reddedilir ve Sam'e geri gönderilir.
        - Eğer hem Sue hem de Jo belgeye onay verirse, onay için Ann'e gönderilir.

    - **Tüm onaylayanlar** – Tüm onaylayanlar belgeyi onaylamalıdırlar. Aksi halde, iş akışı devam edemez. Örneğin, Sam 15.000 USD tutarında bir gider raporu gönderdi. Gider raporu şu an Sue, Jo ve Bill'e atanmıştır. Sue ve Joe belgeye onay verir fakat Bill reddederse, belge reddedilir ve Sam'e geri gönderilir. Eğer Sue, Jo ve Bill'in tamamı belgeye onay verirse, onay için Ann'e gönderilir.

## <a name="specify-when-the-approval-step-is-required"></a>Onay adımının ne zaman gerekli olduğunu belirtin

Onay adımının ne zaman gerekli olduğunu belirtebilirsiniz. Onay adımı her zaman gerekli olabilir veya yalnızca belirli koşullar sağlanırsa gerekli olabilir.

### <a name="the-approval-step-is-always-required"></a>Onay adımı her zaman gereklidir

Onay adımı her zaman gerekli ise, aşağıdaki adımları izleyin.

1. Sol bölmede **Koşul**'u tıklatın.
2. **Bu adımı her zaman çalıştır** seçeneğini belirleyin.

### <a name="the-approval-step-is-required-in-specific-conditions"></a>Onay adımı belirli koşullarda gerekiyor

Yapılandırmakta olduğunuz onay adımı yalnızca belirli koşullar sağlandığında gerekli olabilir. Örneğin, satınalma talebi iş akışı için bir onay adımı yapılandırıyorsanız, onay adımının yalnızca satın alma talebi 10.000 USD'den fazla olduğunu gerçekleşmesini isteyebilirsiniz. Onay adımının ne zaman gerekli olduğunu belirtmek için şu adımları izleyin.

1. Sol bölmede **Koşul**'u tıklatın.
2. **Bu adımı yalnızca aşağıdaki koşul karşılandığında çalıştır** seçeneğini belirleyin.
3. Koşulu girin.
4. Varsa, gerekli ek koşulları girin.
5. Girdiğiniz koşulların doğru biçimde yapılandırıldığını doğrulamak için, aşağıdaki adımları izleyin:

    1. **Sına**'yı tıklatın.
    2. **İş akışını test et** sayfasında, **Koşulu doğrula** alanında, bir kayıt seçin.
    3. **Sına**'yı tıklatın. Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.
    4. **Özellikler** sayfasında geri dönmek için **OK** ya da **İptal Et**'e tıklayın.

## <a name="specify-what-happens-when-the-document-is-overdue"></a>Belgenin vadesi geçtiğinde ne olduğunu belirtin

Eğer bir kullanıcı bu zaman içerisinde bir belge üzerinde eyleme geçmezse, belgenin vadesi geçer. Vadesi geçmiş bir belge ilerletilebilir veya onay için başka bir kullanıcıya otomatik olarak atanabilir. Vadesi geçmiş ise, belgenin üst düzeye ilerletilmesi için aşağıdaki adımları izleyin.

1. Sol bölmede **İlerletilme**'yı tıklatın.
2. İlerletme yolu oluşturmak için **İlerletme yolunu kullan** onay kutusunu seçin. Sistem belgeyi ilerletme yolunda listelenmiş olan kullanıcılara otomatik olarak atar. Örneğin, aşağıdaki tablo bir ilerletme yolunu temsil eder.

    | Seri | İlerletme yolu      |
    |----------|----------------------|
    | 1        | Şu kişiye ata: Donna     |
    | 2        | Şu kişiye ata: Erin      |
    | 3        | Son eylem: Reddet |

    Bu örnekte sistem süresi geçen belgeyi Donna'ya atar. Eğer Donna ayrılan süre içerisinde yanıt vermezse, sistem belgeyi Erin'e atar. Eğer Erin ayrılan süre içerisinde yanıt vermezse, sistem belgeyi reddeder.

3. Bir kullanıcıyı ilerletme yoluna eklemek için **İlerletme ekle**'yi tıklatın. **Atama türü** sekmesinde, aşağıdaki tablodaki seçeneklerden birini seçin ve 4. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.

    <table>
    <thead>
    <tr>
    <th>Seçenek</th>
    <th>Belgenin ilerletildiği kullanıcılar</th>
    <th>Ek adımlar</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hiyerarşi</td>
    <td>Belirli bir kuruluş hiyerarşisindeki kullanıcılar</td>
    <td>
    <ol>
    <li><strong>Hiyerarşi türü</strong> listesindeki <strong>Hiyerarşi seçimi</strong> sekmesinde <strong>Hiyerarşi</strong>'yi seçtikten sonra, belgenin ilerletileceği hiyerarşi türünü seçin.</li>
    <li>Sistemin bu hiyerarşiden kullanıcı adları aralığını alması gerekir. Bu adlar belgenin ilerletilebileceği kullanıcıları temsil eder. Sistemin alacağı adların aralığının başlangıç ve bitiş noktasını belirtmek için aşağıdaki adımları izleyin: <ol>
    <li>Başlangıç noktasını belirtmek için, <strong>Buradan başla:</strong> listesinde bir kişi seçin.</li>
    <li>Bitiş noktasını belirtmek için <strong>Koşul ekle</strong>'yi tıklatın. Daha sonra, sistemin hiyerarşinin neresinde ad almayı durduracağını belirten bir koşul girin.</li>
    </ol>
    </li>
    <li><strong>Hiyerarşi seçenekleri</strong> sekmesinde, aralığın içindeki hangi kullanıcılara belgenin ilerletilmesi gerektiğini belirtin: <ul>
    <li><strong>Alınan tüm kullanıcılara ata</strong> – Belge bu aralıktaki tüm kullanıcılara ilerletilir.</li>
    <li><strong>Yalnızca alınan son kullanıcıya ata</strong> – Belge yalnızca aralıktaki son kullanıcıya ilerletilir.</li>
    <li><strong>Aşağıdaki koşul ile kullanıcıları dışarıda bırakmak</strong> – Belge, aralıkta belirli bir koşulu yerine getiren herhangi bir kullanıcıya ilerletilmez. Koşulu belirtmek için <strong>Koşul ekle</strong>'yi tıklatın.</li>
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
    <li><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm  kullanıcılarını içerir. Belgenin ilerletileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. **Zaman limiti** sekmesinde, **Süre** alnında, kullanıcının onay adımına ulaşan belgeler üzerinde eyleme geçmek üzere ne kadar zamanı olduğunu belirtin. Aşağıdaki seçeneklerden birini belirleyin:

    - **Saatler** – Kullanıcının yanıt vermesi gereken saat sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Günler** – Kullanıcının yanıt vermesi gereken gün sayısını girin. Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.
    - **Haftalar** – Kullanıcının yanıt vermesi gereken hafta sayısını girin.
    - **Aylar** – Kullanıcının yanıt vermesi gereken günü ve haftayı seçin. Örneğin, kullanıcının ayın üçüncü haftasındaki Cuma günü yanıt vermesini isteyebilirsiniz.
    - **Yıllar** – Kullanıcının yanıt vermesi gereken haftayı ve ayı seçin. Örneğin, kullanıcının Aralık ayının üçüncü haftasındaki Cuma günü yanıt vermesini isteyebilirsiniz.

5. İlerletme yoluna eklenecek tüm kullanıcılar için 3. adım ve 4. adımlar arasındaki süreci yineleyin. Kullanıcıların sıralamasını değiştirebilirsiniz.
6. İlerletme yolundaki kullanıcılar verilen süre içinde yanıt vermezlerse, sistem belge üstünde otomatik olarak eylem yapar. Sistemin alacağı eylemi belirtmek için **Eylem** satırını seçin ve sonra **Eylemi bitir** sekmesi üzerinde bir eylem seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]