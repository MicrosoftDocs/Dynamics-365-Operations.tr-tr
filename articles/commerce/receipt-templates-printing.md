---
title: Giriş biçimleri ayarlama ve tasarlama
description: Bu makale makbuz, fatura ve diğer belgelerin nasıl yazdırılacağını belirlemek için form düzenlerinin nasıl değiştirileceğini açıklar. Dynamics 365 Commerce, çeşitli form düzenlerini kolayca oluşturmak ve değiştirmek için kullanabileceğiniz bir form düzeni tasarımcısına sahiptir.
author: rubencdelgado
ms.date: 09/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a2107670cb5dbac3b8f28c4e3caa357102932291
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500183"
---
# <a name="set-up-and-design-receipt-formats"></a>Giriş biçimleri ayarlama ve tasarlama

[!include [banner](includes/banner.md)]

Bu makale makbuz, fatura ve diğer belgelerin nasıl yazdırılacağını belirlemek için form düzenlerinin nasıl değiştirileceğini açıklar. Dynamics 365 Commerce, çeşitli form düzenlerini kolayca oluşturmak ve değiştirmek için kullanabileceğiniz bir form düzeni tasarımcısına sahiptir.

> [!IMPORTANT]
> Retail Modern POS ve Bulut POS'dan alınan girişleri ve diğer belgeleri yazdırmak için form düzenlerini ve giriş profillerini ayarlamanız gerekir. Bir giriş profiline birden çok form düzeni ekleyebilirsiniz.. Daha sonra bir donanım profilini değiştirerek giriş profilini bir yazıcıya atayabilirsiniz.

## <a name="set-up-a-receipt-format"></a>Bir giriş biçimi ayarlama

1. **Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Receipt formats** (Perakende ve ticaret > Kanal kurulumu > POS kurulumu > POS > Giriş biçimleri) menüsüne tıklayın.
2. **Giriş biçimi** sayfasında, yeni bir form düzeni oluşturmak için **Yeni** öğesine tıklayabilir veya mevcut bir form düzeni seçebilirsiniz.
3. **Giriş biçimi** alanına form düzeni için bir tanımlayıcı girin ve sonra bu düzenin kullanıldığı girişin türünü seçin. Ayrıca **Başlık** alanında giriş için bir tanım ve kısa bir ad da girebilirsiniz.
4. **Genel** Hızlı Sekmesinde, yazdırma davranışını tanımlamak için aşağıdaki seçeneklerden birini seçin:

    - **Her zaman yazdır** – Giriş uygun şekilde otomatik olarak yazdırılır.
    - **Yazdırma** – Giriş yazdırılmaz.
    - **Kullanıcıdan istemde bulun** – Kullanıcıdan girişi yazdırması istenir.
    - **Gereken şekilde** – Bu seçenek sadece hediye girişleri için kullanılır. Bu seçenek seçildiğinde, bir hediye girişi gerekiyorsa kullanıcı **Değiştir** sayfasından bir hediye girişini yazdırabilir.

## <a name="print-images"></a>Resimleri yazdırma

Makbuz tasarımcısı bir **Logo** değişkeni içerir. Makbuzlarda yazdırılması gereken bir görüntüyü belirtmek için bu değişkeni kullanabilirsiniz. **Logo** değişkenini kullanarak makbuzlarda yazdırılan görüntüler, tek renkli bit eşlem (.bmp) dosya türleri olmalıdır. Makbuz tasarımcısında bir bitmap görüntüsü belirtilirse ancak makbuz yazıcıya gönderildiğinde yazdırılmazsa bunun nedeni aşağıdaki sorunlardan biri olabilir:

- Dosya boyutu çok büyük veya görüntünün piksel boyutları yazıcıyla uyumlu değil. Bu durumda, görüntü dosyasının çözünürlüğünü veya boyutlarını azaltmayı deneyin.
- Bazı Satış Noktası için Nesne Bağlama ve Katıştırma (OPOS) yazıcı sürücüleri, logo görüntülerini yazdırmak için donanım istasyonlarının kullanıldığı **PrintMemoryBitmap** yöntemini uygulamaz. Bu durumda, ayırdığınız veya paylaştığınız donanım istasyonunun **HardwareStation.Extension.config** dosyasına aşağıdaki bayrağı eklemeyi deneyin:

    `<add name="HardwareStation.UsePrintBitmapMethod" value="true"/>`

## <a name="design-a-receipt-format"></a>Bir giriş biçimi tasarlama

Form belgesinin düzenini grafik olarak oluşturmak için form düzen tasarımcısını kullanın. **Giriş biçimi tasarımcısı** sayfasında üç bölüm bulunur: **Başlık**, **Satırlar** ve **Altbilgi**. Bazı form düzeni türleri, her üç bölümden de öğeleri kullanırken, diğer türler sadece bir veya iki bölümden öğeleri kullanır. Her bölüm için kullanılabilen öğeleri görüntülemek için, sayfanın sol tarafındaki yönlendirme bölümündeki uygun düğmeye tıklayın.

1. **Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Receipt formats** (Perakende ve ticaret > Kanal kurulumu > POS kurulumu > POS > Giriş biçimleri) menüsüne tıklayın.
2. **Giriş biçimi** sayfasında, bir form düzeni seçin ve **Tasarımcı** seçeneğine tıklayın.
3. Commerce tasarımcısı ana bilgisayarını yüklemeye başlamak için **Çalıştır** öğesine tıklayın.
4. Internet Explorer penceresinin altında beliren Bildirim çubuğunda, tek işlemli tasarımcıyı yüklemeye başlamak için **Aç** öğesine tıklayın. (Bildirim çubuğu diğer tarayıcılarda farklı bir konumda görüntülenebilir.) İlerleme göstergesi yükleme işleminin ilerlemesini gösterir.
5. Kurulum tamamlandıktan sonra tasarımcıyı başlatmak için Commerce kullanıcı adınızı ve parolanızı girip **Oturum aç**'a tıklayın.
6. Bilgileriniz doğrulandıktan ve tasarımcı başlatıldıktan sonra, giriş biçimi tasarlamaya veya mevcut bir biçimi değiştirmeye başlayabilirsiniz.
7. Formun öğelerini oluşturmak için, **Başlık**, **Satırlar** veya **Altbilgi** bölümünü seçip, bir öğeyi o bölümden çalışma alanına sürükleyin. Çoğu öğe otomatik olarak veritabanından gelen verilerle doldurulan değişkenleri içerir. **Metin** gibi diğer öğeler size giriş üzerindeki özel metni yazdırma olanağı verir.

    > [!NOTE]
    > Her bölümün kaç satır içerdiğini, o bölümün sağ alt köşesindeki sayıyı ayarlayarak belirleyebilirsiniz. Bir bölümü değiştirmeyi kolaylaştırmak için, bölümün altındaki boyutlandırma çubuğunu sürükleyerek yüksekliğini arttırın. Çalışma alanındaki bölümün yüksekliği, gerçek girişteki satır sayısını etkilemez.

8. Bir öğeyi çalışma alanına sürükledikten sonra, sayfanın altındaki **Nesne bilgisi** bölmesinde o kısmın özelliklerini ayarlayın. Aşağıdaki ayarlardan birini veya birden fazlasını girin:

    - **Hizala** – Alanı **Sola** veya **Sağa** hizalayın.
    - **Dolgu karakteri** – Boşluk karakterini belirleyin. Varsayılan olarak boş bir alan kullanılır, ancak herhangi bir karakter girebilirsiniz.
    - **Önek** – Alanın başında görünen değeri girin. Bu ayar sadece düzenin **Satırlar** bölümünde uygulanır.
    - **Karakterler** – Öğe bir değişken içeriyorsa, alanın içerebileceği maksimum karakter sayısını belirtin. Alandaki metin, belirttiğiniz karakter sayısından uzunsa metin alana sığacak şekilde kesilir.
    - **Değişken** – Öğe bir değişken içeriyorsa ve özelleştirilemiyorsa, bu onay kutusu otomatik olarak seçilir.
    - **Yazı tipi** – Yazı tipi stilini **Normal** veya **Kalın** olarak ayarlayın. Kalın harfler normal harflerden iki kat daha fazla yer kaplar. Bu yüzden, bazı karakterler kesilebilir.
    - **Yazı tipi boyutu** – Yazı tipi boyutunu **Normal** veya **Büyük** olarak ayarlayın. Büyük harfler normal harflerden iki kat daha büyüktür. Bu nedenle, büyük harfler kullanmak makbuzda harflerin üst üste gelmesine neden olabilir.
    - **Si** – Seçili bölümü form düzeninden kaldırmak için bu düğmeyi tıklatın.

## <a name="assign-receipt-profiles"></a>Giriş profilleri atama

Giriş profilleri donanım profili yoluyla doğrudan yazıcılara atanır.

1. Donanım profilini **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **Donanım profili** menüsüne tıklayarak açın.
2. Yazıcıyı seçin ve **Giriş profili** alanında kayıtta kullanılacak fatura profilini atayın.

> [!NOTE]
> İki yazıcı kullanılıyorsa, standart 40 sütunluk termal faturaları yazdırmak için bir yazıcı kullanılabilir. İkinci yazıcı normalde daha fazla bilgi gerektiren tam sayfa giriş türlerini yazdırmak için kullanılır. Bu giriş türleri arasında müşteri sipariş girişleri ve müşteri faturaları bulunur.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
