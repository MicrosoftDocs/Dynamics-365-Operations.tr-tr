---
title: Müşteri yaşlandırma anlık görüntüleri
description: Bu makalede, müşteri yaşlandırma anlık görüntüleriyle ilgili bilgiler sağlanmaktadır. Yaşlandırma anlık görüntüsü, bir müşteri grubunun belirli bir zamandaki yaşlandırılmış bakiyesini hesaplar.
author: JodiChristiansen
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: 88145cdccfe3f1d0d3de4e31dfa519b27df6550a
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643698"
---
# <a name="customer-aging-snapshots"></a>Müşteri yaşlandırma anlık görüntüleri

[!include [banner](../includes/banner.md)]

Bu makalede, müşteri yaşlandırma anlık görüntüleriyle ilgili bilgiler sağlanmaktadır. Bir yaşlandırma anlık görüntüsü, bir müşteri grubunun bir zamandaki yaşlandırılmış bakiyesini hesaplar. Tüm müşteriler veya bir müşteri havuzundaki müşteriler için yaşlandırma anlık görüntüsü oluşturabilirsiniz.

Yaşlandırma anlık görüntüsü bilgileri,**Yaşlandırılmış bakiyeler** listesi sayfası ve **Tahsilatlar** sayfasında görüntülenir. **Yaşlandırılmış bakiyeler** listesini kullanmadan önce bir yaşlandırma anlık görüntüsünü oluşturmanız gerekir. Liste sayfası, sadece yaşlandırma anlık görüntüsü oluşturulan müşterileri listeler.

**Müşteri alacak ve tahsilatları** çalışma alanında aynı zamanda müşteri yaşlandırması da görüntülenir. Daha fazla bilgi için bkz. [Power BI içerikleri alacak ve tahsilatlar yönetimi](credit-collections-power-bi.md).

> [!NOTE]
> Yaşlandırma anlık görüntüsü oluşturmak için gereken süreyi azaltmak için **Özellik yönetimi** çalışma alanındaki şu özellikleri etkinleştirin: **Müşteri yaşlandırma performansı geliştirmesi** 
> **Müşteri havuzları ile müşteri yaşlandırma performansı geliştirmesi**  
> Her iki özellik de etkin olduğu zaman **Müşteri havuzları**, yaşlandırma anlık görüntüsü oluştururken kullanılabilir. 

Bir müşteri yaşlandırma anlık görüntüsü oluşturduğunuzda, bununla ilgili bilgileri girmek için aşağıdaki alanları kullanın:

- **Yaşlandırma dönemi tanımı** – Yaşlandırma anlık görüntüsü için yaşlandırma dönemi tanımını seçin. Her yaşlandırma dönemi için bir yaşlandırma anlık görüntü alabilirsiniz. Yaşlandırma anlık görüntüsünün ve yaşlandırma dönemi tanımının ayrı olarak oluşturulması gerekir.
- **Havuz Kimliği** – Bu alan isteğe bağlıdır. Yaşlandırma anlık görüntüsünde işlenmesi gereken müşteri kümesini tanımlamak için bir havuz kullanabilirsiniz. Bu alanda bir müşteri havuzu seçerseniz, yaşlandırma anlık görüntüsü yalnızca bu müşteri havuzunun bir parçası olan müşteri hesapları için oluşturulur. Seçili müşteri havuzu **Yaşlandırma anlık görüntüsü** türünde olmalıdır. Bu alanı boş bırakırsanız, tüm müşteri hesapları için bir yaşlandırma anlık görüntüsü oluşturulur.


- **Ölçüt** – Yaşlandırma anlık görüntüsü, seçtiğiniz tarihe göre yaşlandırır:

    - **Hareketi tarihi** – Her bir hareket, hareket tarihine göre yaşlandırılır.
    - **Vade tarihi** – Her bir hareket, vade tarihine göre yaşlandırılır.
    - **Belge tarihi** – Her bir hareket, belge tarihine göre yaşlandırılır.

- **Yaşlandırma başlama tarihi** Yaşlandırma anlık görüntüsü için **Geçerli tarih** alanında kullanılacak tarihi seçin. Ardından, yaşlandırma dönemleri bu tarih temel alınarak hesaplanır. 

    - **Bugünün tarihi** – Sistem tarihini kullanın. İşlem, tekrarlayan bir toplu işte çalıştırmak üzere ayarlanırsa bu seçeneği kullanın. Ardından, toplu iş her çalıştırıldığında, söz konusu çalıştırmanın sistem tarihi kullanılır.
    - **Seçili tarih** – Belirttiğiniz tarihi kullanın. Bu seçeneği belirlediğinizde, bir yaşlandırma tarihi de girmeniz gerekir.

   Örneğin, geçerli yaşlandırma süresi 30 gündür. Bu alanda **Bugünün tarihi**'ni seçerseniz, geçerli yaşlandırma dönemi bugünün tarihinde başlar ve önceki 29 günü de içerir. Bu alanda **Seçili tarih**'i seçip bir tarih girerseniz, geçerli yaşlandırma dönemi belirtilen tarihte başlar ve önceki 29 günü de içerir.

- **Tahsilat durumunu güncelleştir** – Yaşlandırma tarihi, **Ödeme taahhüdü tarihi** alanındaki tarihin ileri bir tarihindeyse **Tahsilatlar** sayfasındaki tahsilat durumunu **Ödeme taahhüdü**'nden **Ödeme taahhüdü yerine getirilmedi**'ye güncelleştirmek için bu seçeneği **Evet** olarak ayarlayın. **Tahsilatlar** sayfasında tahsilat durumunu değiştirmeden bırakmak için bu seçeneği **Hayır** olarak belirleyin.
- **Bakiyesi sıfır olan müşterileri dahil et** – Bakiyesinden bağımsız olarak tüm müşterileri dahil etmek için bu seçeneği **Evet** olarak ayarlayın. Tüm müşterileri dahil etmeniz halinde **Müşteri yaşlandırma performansı geliştirmesi** ve **Müşteri havuzları ile müşteri yaşlandırma performansı geliştirmesi** özelliklerini etkinleştirmenizi öneririz. Yalnızca bakiyesi olan müşterileri dahil etmek için bu seçeneği **Hayır** olarak ayarlayın. Bakiyesi olmayan müşteriler atlandığı için bu ayar, performansı hızlandırmaya yardımcı olur.
- **Yaşlandırma sırasında kredi limiti hesaplamalarını atla** - Bu seçenek, **Evet** olarak ayarlandıysa yaşlandırma süreci, her bir müşteri için **Sevk irsaliyesi alt toplam** tutarını, **Açık sipariş alt toplam** tutarını ve **Kullanılabilir kredi** değerini yeniden hesaplamaz. Bu bakiyeler, **Kredi limiti** altındaki bilgi kutusunda **Yaşlandırılmış bakiyeler** sayfasında gösterilir. Yaşlandırma işlemi sırasında performansı hızlandırmak için bu seçeneği **Evet** olarak ayarlayın. Yaşlandırma işlemini çalıştırırken bakiyeleri yeniden hesaplamak için **Hayır** olarak ayarlayın. 
- **Şirket aralığı** – **Şirket aralığı** sekmesinde, yaşlandırma anlık görüntüsüne dahil edilecek tüzel kişilikleri (şirketler) seçin. Yalnızca merkezi ödemeler için ayarlanmış tüzel kişilikler seçilebilir. Ardından, seçilen tüzel kişiliklerindeki hareketler, tüm bu tüzel kişiliklerde aynı taraf koduna sahip müşteriler için yaşlandırma dönemlerine dahil edilir. Para birimi miktarları, yaşlandırma anlık görüntüsünü oluşturduğunuzda oturum açtığınız tüzel kişiliğin para birimine dönüştürülür.

Bu işlemi, toplu işte çalışacak şekilde zamanlamanızı öneririz.

> [!NOTE]
> Yaşlandırma anlık görüntüleri oluşturulurken toplu iş performansını geliştirmeye yardımcı olmak için, **Alacak hesapları parametreleri** sayfasının **Tahsilatlar** sekmesindeki **Tahsilat varsayılanları** hızlı sekmesinde bulunan **Maksimum toplu iş sayısı** alanına bir sayı girin. **Müşteri bakiyelerini yaşlandır** alanında **12** ile **20** arasında bir değer ile başlamanızı ve sonra durumunuza göre işlemi optimize etmek için bu değeri ayarlamanızı öneriyoruz. Performansı etkileyebileceği için bu değeri **30**'dan büyük bir değere ayarlamanız önerilmez. 

