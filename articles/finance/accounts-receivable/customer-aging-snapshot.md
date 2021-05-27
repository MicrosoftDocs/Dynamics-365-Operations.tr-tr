---
title: Müşteri yaşlandırma anlık görüntüleri
description: Bu konu müşteri yaşlandırma anlık görüntüleriyle ilgili bilgiler sağlar. Bir yaşlandırma anlık görüntüsü, bir müşteri grubunun bir zamandaki yaşlandırılmış bakiyesini hesaplar.
author: JodiChristiansen
ms.date: 05/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7761366c0372c105ecbd4281c7bafa44bf6cf7b5
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039939"
---
# <a name="customer-aging-snapshots"></a>Müşteri yaşlandırma anlık görüntüleri

[!include [banner](../includes/banner.md)]

Bu konu müşteri yaşlandırma anlık görüntüleriyle ilgili bilgiler sağlar. Bir yaşlandırma anlık görüntüsü, bir müşteri grubunun bir zamandaki yaşlandırılmış bakiyesini hesaplar. Tüm müşteriler veya bir müşteri havuzundaki müşteriler için yaşlandırma anlık görüntüsü oluşturabilirsiniz.

Yaşlandırma anlık görüntüsü bilgileri,**Yaşlandırılmış bakiyeler** listesi sayfası ve **Tahsilatlar** sayfasında görüntülenir. **Yaşlandırılmış bakiyeler** listesini kullanmadan önce bir yaşlandırma anlık görüntüsünü oluşturmanız gerekir. Liste sayfası, sadece yaşlandırma anlık görüntüsü oluşturulan müşterileri listeler.

> [!NOTE]
> Yaşlandırma anlık görüntüsü oluşturmak için gereken süreyi azaltmak için, **Özellik yönetimi** çalışma alanındaki **Müşteri yaşlandırma performansı geliştirmesi** özelliğini etkinleştirin. Ancak, bu özellik etkinleştirildiğinde müşteri havuzlarını kullanmayın. Bir müşteri havuzu seçiliyse özellik çalışmaz ancak yine de yaşlandırma anlık görüntüsü oluşturabilirsiniz.

Bir müşteri yaşlandırma anlık görüntüsü oluşturduğunuzda, bununla ilgili bilgileri girmek için aşağıdaki alanları kullanın:

- **Yaşlandırma dönemi tanımı** – Yaşlandırma anlık görüntüsü için yaşlandırma dönemi tanımını seçin. Her yaşlandırma dönemi için bir yaşlandırma anlık görüntü alabilirsiniz. Yaşlandırma anlık görüntüsünün ve yaşlandırma dönemi tanımının ayrı olarak oluşturulması gerekir.
- **Havuz Kimliği** – Bu alan isteğe bağlıdır. Yaşlandırma anlık görüntüsünde işlenmesi gereken müşteri kümesini tanımlamak için bir havuz kullanabilirsiniz. Bu alanda bir müşteri havuzu seçerseniz, yaşlandırma anlık görüntüsü yalnızca bu müşteri havuzunun bir parçası olan müşteri hesapları için oluşturulur. Seçili müşteri havuzu **Yaşlandırma anlık görüntüsü** türünde olmalıdır. Bu alanı boş bırakırsanız, tüm müşteri hesapları için bir yaşlandırma anlık görüntüsü oluşturulur.

    > [!NOTE]
    > **Müşteri yaşlandırma performansı geliştirmesi** özelliği açıksa, bir müşteri havuzu seçmeyin.

- **Ölçüt** – Yaşlandırma anlık görüntüsü, seçtiğiniz tarihe göre yaşlandırır:

    - **Hareketi tarihi** – Her bir hareket, hareket tarihine göre yaşlandırılır.
    - **Vade tarihi** – Her bir hareket, vade tarihine göre yaşlandırılır.
    - **Belge tarihi** – Her bir hareket, belge tarihine göre yaşlandırılır.

- **Yaşlandırma başlama tarihi** Yaşlandırma anlık görüntüsü için **Geçerli tarih** alanında kullanılacak tarihi seçin. Ardından, yaşlandırma dönemleri bu tarih temel alınarak hesaplanır. 

    - **Bugünün tarihi** – Sistem tarihini kullanın. İşlem, tekrarlayan bir toplu işte çalıştırmak üzere ayarlanırsa bu seçeneği kullanın. Ardından, toplu iş her çalıştırıldığında, söz konusu çalıştırmanın sistem tarihi kullanılır.
    - **Seçili tarih** – Belirttiğiniz tarihi kullanın. Bu seçeneği belirlediğinizde, bir yaşlandırma tarihi de girmeniz gerekir.

    Örneğin, geçerli yaşlandırma süresi 30 gündür. Bu alanda **Bugünün tarihi**'ni seçerseniz, geçerli yaşlandırma dönemi bugünün tarihinde başlar ve önceki 29 günü de içerir. Bu alanda **Seçili tarih**'i seçip bir tarih girerseniz, geçerli yaşlandırma dönemi belirtilen tarihte başlar ve önceki 29 günü de içerir.

- **Tahsilat durumunu güncelleştir** – Yaşlandırma tarihi, **Ödeme taahhüdü tarihi** alanındaki tarihin ileri bir tarihindeyse **Tahsilatlar** sayfasındaki tahsilat durumunu **Ödeme taahhüdü**'nden **Ödeme taahhüdü yerine getirilmedi**'ye güncelleştirmek için bu seçeneği **Evet** olarak ayarlayın. **Tahsilatlar** sayfasında tahsilat durumunu değiştirmeden bırakmak için bu seçeneği **Hayır** olarak belirleyin.
- **Bakiyesi sıfır olan müşterileri dahil et** – Bakiyesinden bağımsız olarak tüm müşterileri dahil etmek için bu seçeneği **Evet** olarak ayarlayın. Tüm müşterileri dahil ederseniz, **Müşteri yaşlandırma performansı geliştirme** özelliğini açmanızı ve müşteri havuzları kullanmamanızı öneririz. Yalnızca bakiyesi olan müşterileri dahil etmek için bu seçeneği **Hayır** olarak ayarlayın. Bakiyesi olmayan müşteriler atlandığından, bu ayar performansı hızlandırmaya yardımcı olur.
- **Şirket aralığı** – **Şirket aralığı** sekmesinde, yaşlandırma anlık görüntüsüne dahil edilecek tüzel kişilikleri (şirketler) seçin. Yalnızca merkezi ödemeler için ayarlanmış tüzel kişilikler seçilebilir. Ardından, seçilen tüzel kişiliklerindeki hareketler, tüm bu tüzel kişiliklerde aynı taraf koduna sahip müşteriler için yaşlandırma dönemlerine dahil edilir. Para birimi miktarları, yaşlandırma anlık görüntüsünü oluşturduğunuzda oturum açtığınız tüzel kişiliğin para birimine dönüştürülür.

Bu işlemi, toplu işte çalışacak şekilde zamanlamanızı öneririz.

> [!NOTE]
> Yaşlandırma anlık görüntüleri oluşturulurken toplu iş performansını geliştirmeye yardımcı olmak için, **Alacak hesapları parametreleri** sayfasının **Tahsilatlar** sekmesindeki **Tahsilat varsayılanları** hızlı sekmesinde bulunan **Maksimum toplu iş sayısı** alanına bir sayı girin. **Müşteri bakiyelerini yaşlandır** alanında, varsayılan değer olan **100** ile başlamanızı ve sonrasında durumunuza göre işlemi optimize etmek için bu değeri ayarlamanız önerilir.

**Müşteri alacak ve tahsilatları** çalışma alanında aynı zamanda müşteri yaşlandırması da görüntülenir. Daha fazla bilgi için bkz. [Power BI içerikleri alacak ve tahsilatlar yönetimi](credit-collections-power-bi.md).
