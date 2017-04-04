---
title: "Ambar mobil cihazı görüntüleme ayarları"
description: "Bu makale, mobil cihaz ekranın görünümünün nasıl ayarlandığını ve bu düğmelerin denetimi için klavye kısayollarının nasıl eşleneceğini açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 721b293d1f8c76458ca510732f9bb94f003ac6e3
ms.lasthandoff: 03/31/2017


---

# <a name="warehouse-mobile-device-display-settings"></a>Ambar mobil cihazı görüntüleme ayarları

Bu makale, mobil cihaz ekranın görünümünün nasıl ayarlandığını ve bu düğmelerin denetimi için klavye kısayollarının nasıl eşleneceğini açıklar. 

Bu makale, Ambar yönetimindeki "gelişmiş depolama" özellikleri için geçerlidir. Mobil aygıtlar ambar çalışanlarının gerçekleştirdiği görevlerin çoğu için kullanılabilir.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Stillerini belirtin ve klavye kısayolları eşleyin
Taşınabilir aygıt yapılandırma işleminin bir parçası olarak, mobil cihazlar için farklı düzenler tanımlayabilirsiniz. Bunu yapmak için Basamaklı Stil Sayfaları (CSS) dosyası ve Active Server Sayfası Uzantısı (ASPX) dosya adını bilmeniz gerekir. Varsayılan dosyaları Ambar mobil aygıtlar Portal yüklemesinin bir parçası olarak yüklenir. Dosya adlarını bilmiyorsanız, sistem yöneticinize başvurun. Yeni bir stili **mobil aygıt görüntü ayarlarını** sayfasında tanımlayabilirsiniz:

-    **CSS dosyası** alanına CSS dosyası için bir ad girin. .css dosya adı uzantısını dahil edin.
-   **mobil aygıt görüntü ayarları görünümünü** alanında, ASPX dosyası belirtin. .aspx dosya adı uzantısını **eklemeyin**.

Internet Information Services (IIS) uygulama yükleyebilecek şekilde CSS ve ASPX dosyaları belirli bir dizinde yer almalıdır. Mobil aygıt işlevini farklı tarayıcılarda veya farklı düzen denetimi gerektiren çeşitli donanım üzerinde çalıştırıyorsanız, farklı CSS dosyaları tanımlamak yararlı olabilir. Arka plan rengi, yazı tipi ve metin için yazı tipi boyutu ve genişliği ve düğmelerin davranışı gibi basit ayarları kolayca farklı CSS dosyalarının kullanımıyla denetlenebilir. ASPX dosyası mobil site sunucu tarafı ASP.NET uygulamasında görüntülemek için kullanılır. Dosya HTML genel yapısını nasıl düzenlendiği denetler. Bu işlev yalnızca, HTML ve JavaScript ile ciddi yapısal sorunlar varsa ve bu kodu, belirli aygıtlar için değiştirmeniz gerekirse özelleştirmek için iyi bir fikirdir. mobil aygıt sayfaya üzerinde HTML denetimleri Klavye kısayollarına eşlemek için **mobil aygıt görüntü ayarlarını** sayfasında **klavye kısayolu** alanında, anahtarlar için sayısal kodları atayın. **Klavye kısayolları için kodları görüntüle** menüsünü mobil aygıtta sayısal karakter kodlarını bulmak için kullanabilirsiniz. Eşlemelerin, kullanılan donanım bağlı olarak farklı olabileceğini unutmayın. Eşlemeyi oluşturmak için aşağıdaki söz dizimini kullanmanız gerekir:

&lt;Denetim adı&gt;(&lt;anahtar adı&gt;) =&lt;tuş kodu&gt;;

Sözdizimi bölümlerinin açıklaması aşağıdadır:

-   **&lt;Denetim adı&gt;** – HTML biçiminde işlenir (örneğin, bir düğme gibi) denetim adı.
-   **(&lt;anahtar adı&gt;) ** – İçin kısayol oluşturuyorsanız klavye tuşu adı.
-   **&lt;Tuş kodu&gt;** – sayısal karakter kodu için kısayol tuşu olarak kullanmak anahtar.

Aşağıda bir örnek verilmiştir:

İptal et (Esc) = 27; Tam (F2)=113

**iptal** düğmesi dahil tüm sayfalarda, bu metin düğmesi olacaktır:

**(Esc) İptal Et**

Klavyenizdeki Esc tuşuna basmak **iptal** düğmesini etkinleştirir. Belirli bir aygıt için stil ve klavye kısayol ayarları uygulamak için **ölçüt** alanında bir eşleme oluşturmanız gerekir. Eşleme oluşturmak için .NET normal ifade kullanmanız gerekir ve ifadenin bir düşey ayrılmış çubuk (|), üç bölümde oluşması gerekir, aşağıda gösterildiği gibi:

Request.UserHostAddress=&lt;kullanıcı ana bilgisayar adresi&gt;| Ana bilgisayar adı =&lt;kullanıcı ana bilgisayar adı&gt;| Request.UserAgent=&lt;kullanıcı aracısı&gt;

İfade bölümlerinin açıklaması aşağıdadır:

-   **&lt;Kullanıcı ana bilgisayar adresi&gt;** – isteyicinin IP adresiyle eşleşen bir .NET normal ifade.
-   **&lt;Kullanıcı ana bilgisayar adı&gt;** – isteyicinin ağ adıyla bir .NET normal ifade.
-   **&lt;Kullanıcı Aracısı&gt;** – isteyicinin kullandığı tarayıcının tanımlayıcısı ile eşleşirse bir .NET normal ifade.

Aşağıdaki örnek, kullanılacak Internet Explorer 8 etkinleştirir:

Request.UserHostAddress=. \*| Ana bilgisayar adı =. \*| Request.UserAgent=MSIE\\s8\\.0

Mobil aygıt üzerindeki **görüntü ayarları için sunucu yapılandırmasını görüntüleme** menüsünü kurulum hakkında bilgi bulmak için kullanabilirsiniz.

## <a name="define-text-colors-for-messages"></a>İletiler için metin renkleri tanımla
**mobil aygıta metin renkleri** sayfasını kullanarak hata iletileri gibi sistem tarafından oluşturulan iletilerde kullanılan çeşitli renkleri kontrol edebilirsiniz. Örneğin, metin rengi amaç veya iletinin önem derecesini belirtebilir. Aşağıdaki ileti tipleri gösterilir:

| İleti türü | Açıklama                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Varsayılan Değer      | Varsayılan iletiler tüm iletiler için Ambar Mobil Aygıt Portal CSS dosyası tarafından tanımlanan varsayılan renk ayarları kullanır.                                                   |
| Hatalı        | Hata iletileri kullanıcının devam etmeden önce çözümlemesi gereken bir sorunu gösterir.                                                                                             |
| Başarılı      | Başarı iletileri bir eylem başarılı olduğunu onaylar.                                                                                                                                |
| Uyarı      | Uyarı iletileri, çalışana bir sorun olup olmadığını ya da çalışan devam ederse bir sorun olabileceğini bildirir. Ancak, çalışan devam etmek için bu sorunu çözmek zorunda değildir. |

Renk seçmek için **renk seç** sayfasın, paleti tıklatın veya onaltılık renk kodunu yazın.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>Mobil aygıtlarda kullanılacak tarih biçimi tanımla
Her yükleme için kabul edilen tarih biçimleri listesi genişletebilirsiniz. Bu özellik, örneğin, bir mobil aygıtta tarihleri girmek işçi daha kolay anlaşılır biçimde sağlamak istiyorsanız, yararlı olabilir. Varsayılan biçim kullanıcının varsayılan dili tarafından belirlenir, **dil** alanında **kullanıcı seçenekleri** sayfasında belirtilir. (Aynı sayfada aynı zamanda bir çalışan belirli ambar çalışma kullanıcı ile ilişkilendirmek için kullanılır.) **Not:** ambar mobil aygıtlar Portal ayarını kullanmak olmayan **tarih, saat ve sayı biçimini** alanına **dil ve bölge tercihleri** sayfa. Tarih biçimini değiştirmek için Microsoft .NET Framework normal ifadeleri hakkında bilgi sahibi olmanız gerekir. Daha fazla bilgi için bkz: [.NET Framework Normal İfadeleri](http://go.microsoft.com/fwlink/?LinkId=391260). Tarih biçimlerini tanımlamak için içerik bulunan Dates.ini dosyasını düzenleme\\ayarları\\ambar mobil aygıtlar Portal sunucu üzerinde Dates.ini. Bu dosya, tarih biçimini belirtmek için .NET normal ifadeler kullanır. Normal ifade, aşağıdaki örnekte gösterildiği gibi gün, ay ve yıl (GGAAYY) için adlı gruplar oluşturan alt ifadeler içermelidir:

^(? &lt;day&gt;\\d{2})(?&lt; month&gt;\\d{2})(?&lt; yıl&gt;\\d {2}) $

Her alt ifade iki basamaklı gün ve ay, yıl için bir ila dört basamak gerektirir. Örneğin, aşağıdaki alt ifade bir yıl için adlandırılmış bir grup tanımlar ve en az iki basamak veya en çok dört basamak gerektirir:

(? &lt;year&gt;\\d{2,4})

Aynı dosyada birden çok ifade belirtebilirsiniz. Her deyim, ayrı bir satırda olmalıdır. Eşleşen ilk ifade tarih ayrıştırmak için kullanılır.

<a name="see-also"></a>Ayrıca bkz.
--------

[Configuration of mobile devices for warehouse work](configure-mobile-devices-warehouse.md)


