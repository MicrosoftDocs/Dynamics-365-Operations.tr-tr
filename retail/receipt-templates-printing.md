---
title: "Giriş şablonları ve yazdırma"
description: "Bu makale makbuz, fatura ve diğer belgelerin nasıl yazdırılacağını belirlemek için form düzenlerinin nasıl değiştirileceğini açıklar. Operasyon - 365 Microsoft Dynamics Retail kolayca oluşturmak ve çeşitli form düzenlerini değiştirmek için kullanabileceğiniz bir form düzeni tasarımcısı içerir."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabaacbc7187b38a1745c2139a9eb7760f2be987
ms.lasthandoff: 03/31/2017


---

# <a name="receipt-templates-and-printing"></a>Giriş şablonları ve yazdırma

Bu makale makbuz, fatura ve diğer belgelerin nasıl yazdırılacağını belirlemek için form düzenlerinin nasıl değiştirileceğini açıklar. Operasyon - 365 Microsoft Dynamics Retail kolayca oluşturmak ve çeşitli form düzenlerini değiştirmek için kullanabileceğiniz bir form düzeni tasarımcısı içerir.

**Önemli:** form düzenlerini ayarlama ve Modern POS perakende ve bulut POS giriş ve diğer belgeleri yazdırmak için profilleri giriş gerekir. Birden çok form düzeni bir makbuz profiline ekleyebilirsiniz. Daha sonra bir donanım profilini değiştirerek giriş profilini bir yazıcıya atayabilirsiniz.

## <a name="set-up-a-receipt-format"></a>Bir giriş biçimi ayarlama
1.  ' I **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS**&gt;**giriş biçimleri**.
2.  **Giriş biçimi** sayfasında, yeni bir form düzeni oluşturmak için **Yeni** öğesine tıklayabilir veya mevcut bir form düzeni seçebilirsiniz.
3.  **Giriş biçimi** alanına form düzeni için bir tanımlayıcı girin ve sonra bu düzenin kullanıldığı girişin türünü seçin. Ayrıca **Başlık** alanında giriş için bir tanım ve kısa bir ad da girebilirsiniz.
4.  **Genel** Hızlı Sekmesinde, yazdırma davranışını tanımlamak için aşağıdaki seçeneklerden birini seçin:
    -   **Her zaman yazdır** – Giriş uygun şekilde otomatik olarak yazdırılır.
    -   **Yazdırma** – Giriş yazdırılmaz.
    -   **Kullanıcıdan istemde bulun** – Kullanıcıdan girişi yazdırması istenir.
    -   **Gereken şekilde** – Bu seçenek sadece hediye girişleri için kullanılır. Bu seçenek seçildiğinde, bir hediye girişi gerekiyorsa kullanıcı **Değiştir** sayfasından bir hediye girişini yazdırabilir.

## <a name="design-a-receipt-format"></a>Bir giriş biçimi tasarlama
Form belgesinin düzenini grafik olarak oluşturmak için form düzen tasarımcısını kullanın. **Giriş biçimi tasarımcısı** sayfasında üç bölüm bulunur: **Başlık**, **Satırlar** ve **Altbilgi**. Bazı form düzeni türleri, her üç bölümden de öğeleri kullanırken, diğer türler sadece bir veya iki bölümden öğeleri kullanır. Her bölüm için kullanılabilen öğeleri görüntülemek için, sayfanın sol tarafındaki yönlendirme bölümündeki uygun düğmeye tıklayın.

1.  ' I **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS**&gt;**giriş biçimleri**.
2.  **Giriş biçimi** sayfasında, bir form düzeni seçin ve **Tasarımcı** seçeneğine tıklayın.
3.  Perakende tasarımcısı ana bilgisayarını yüklemeye başlamak için **Çalıştır** öğesine tıklayın.
4.  Internet Explorer penceresinin altında beliren Bildirim çubuğunda, tek işlemli tasarımcıyı kurmaya başlamak için **Aç** öğesine tıklayın. (Bildirim çubuğunu diğer tarayıcılarda farklı bir konumda görüntülenebilir.) İlerleme göstergesinin yükleme işleminin ilerlemesini gösterir.
5.  Yükleme tamamlandıktan sonra Dynamics 365 işlemleri kullanıcı adını ve parolasını girin ve'ı **oturum** Tasarımcısı'nı başlatmak için.
6.  Bilgileriniz doğrulandıktan ve tasarımcı başlatıldıktan sonra, giriş biçimi tasarlamaya veya mevcut bir biçimi değiştirmeye başlayabilirsiniz.
7.  Formun öğelerini oluşturmak için, **Başlık**, **Satırlar** veya **Altbilgi** bölümünü seçip, bir öğeyi o bölümden çalışma alanına sürükleyin. Çoğu öğe otomatik olarak veritabanından gelen verilerle doldurulan değişkenleri içerir. **Metin** gibi diğer öğeler size giriş üzerindeki özel metni yazdırma olanağı verir. **Not:** Her bölümün kaç satır içerdiğini, o bölümün sağ alt köşesindeki sayıyı ayarlayarak belirleyebilirsiniz. Bir bölümü değiştirmeyi kolaylaştırmak için, bölümün altındaki boyutlandırma çubuğunu sürükleyerek yüksekliğini arttırın. Çalışma alanındaki bölümün yüksekliği, gerçek girişteki satır sayısını etkilemez.
8.  Bir öğeyi çalışma alanına sürükledikten sonra, sayfanın altındaki **Nesne bilgisi **bölmesinde o kısmın özelliklerini ayarlayın. Aşağıdaki ayarlardan birini veya birden fazlasını girin:
    -   **Hizala** – Alanı **Sola** veya **Sağa** hizalayın.
    -   **Dolgu karakteri** – Boşluk karakterini belirleyin. Varsayılan olarak boş bir alan kullanılır, ancak herhangi bir karakter girebilirsiniz.
    -   **Önek** – Alanın başında görünen değeri girin. Bu ayar sadece düzenin **Satırlar **bölümünde uygulanır.
    -   **Karakterler** – Öğe bir değişken içeriyorsa, alanın içerebileceği maksimum karakter sayısını belirtin. Alandaki metin, belirttiğiniz karakter sayısından uzunsa, metin alana sığacak şekilde kesilir.
    -   **Değişken** – Öğe bir değişken içeriyorsa ve özelleştirilemiyorsa, bu onay kutusu otomatik olarak seçilir.
    -   **Yazı tipi** – Yazı tipi stilini **Normal** veya **Kalın** olarak ayarlayın. Kalın harfler normal harflerden iki kat daha fazla yer kaplar. Bu yüzden, bazı karakterler kesilebilir.
    -   **Si** – Seçili bölümü form düzeninden kaldırmak için bu düğmeyi tıklatın.

## <a name="assign-receipt-profiles"></a>Giriş profilleri atama
Giriş profilleri donanım profili yoluyla doğrudan yazıcılara atanır.

1.  Donanım profili tıklatarak **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS profilleri**&gt;**donanım profili**.
2.  Yazıcıyı seçin ve **Giriş profili **alanında kayıtta kullanılacak fatura profilini atayın.

**Not:** İki yazıcı kullanılıyorsa, standart 40 sütunluk termal faturaları yazdırmak için bir yazıcı kullanılabilir. İkinci yazıcı normalde daha fazla bilgi gerektiren tam sayfa giriş türlerini yazdırmak için kullanılır. Bu giriş türleri arasında müşteri sipariş girişleri ve müşteri faturaları bulunur.


