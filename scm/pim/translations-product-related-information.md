---
title: "Çevirileri ürün ile ilgili sık sorulan sorular"
description: "Bu konuda, ürünler, ürün boyut değerleri ve ürün öznitelikleri için çevirilerin nasıl yönetileceğini açıklanır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a9c991a5afaebd10b8812dfc1d67120ed4ebdfd2
ms.lasthandoff: 03/31/2017


---

# <a name="product-related-translations-faq"></a>Çevirileri ürün ile ilgili sık sorulan sorular

Bu konuda, ürünler, ürün boyut değerleri ve ürün öznitelikleri için çevirilerin nasıl yönetileceğini açıklanır. 

<a name="what-product-related-data-can-be-translated"></a>Ürünle ilgili hangi veriler çevrilebilir?
--------------------------------------------

Ürünle ilgili aşağıdaki bilgilerin çevirilerini oluşturabilirsiniz:
-   Ürün adları ve açıklamaları.
-   Ürün öznitelik değerlerinin açıklamaları, kolay adları ve yardım metni.
-   Ürün boyutu değerlerinin adları ve açıklamaları.

Ürünle ilgili bilgileri, **Metin çevirisi** sayfasında kullanılabilir olan tüm dillere çevirebilirsiniz. Daha fazla bilgi için **Ürünle ilgili bilgilerin çevirilerini nasıl oluştururum** bölümüne bakın.

## <a name="where-can-i-view-the-translated-information"></a>Çevrilmiş bilgileri nerede görüntüleyebilirim?
Ürünle ilgili bilgilerin çevirilerini, fatura gibi çevirilerin kullanılabilir olduğu bir dili kullanan her türlü harici kaynak belgesinde görüntüleyebilirsiniz.

## <a name="how-do-i-create-translations-for-productrelated-information"></a>Productrelated bilgi için çeviriler nasıl oluşturulur?
Ürün için çeviriler oluşturmak için şu adımları izleyin:
1.  ' I **ürün bilgi yönetimi**&gt;**ortak**&gt;**ürünleri piyasaya**.
2.  Bir ürün seçin ve eylem bölmesi içinde **dil** tıklatın, grup **çevirileri**.
3.  **Metin çevirisi** sayfasında **Dil** alanında, bir dil seçin. Daha fazla dil eklemek için Genişlet **dil** alan ve'ı **Tamam**.
4.  **Çevrilmiş metin** grubunda **Açıklama** ve **Ürün adı** alanlarında çevirileri girin.

Ürün öznitelikleri için çeviriler oluşturmak üzere şu adımları izleyin:
1.  ' I **ürün bilgi yönetimi**&gt;**ortak**&gt;**ürünleri piyasaya**.
2.  **Kurulum** altında **Öznitelikler**'e ve ardından **Öznitelikler**'e tıklayın.
3.  **Öznitelikler** sayfasında **Çevir**'e tıklayın.
4.  **Metin çevirisi** sayfasında **Dil** alanında, bir dil seçin. Daha fazla dil eklemek için Genişlet **dil** alan ve'ı **Tamam**.
5.  **Çevrilmiş metin** grubunda **Açıklama**, **Kolay ad** ve **Yardım metni** alanlarında çevirileri girin.

Ürün boyutu değerleri için çeviriler oluşturmak üzere şu adımları izleyin:
1.  ' I **ürün bilgi yönetimi**&gt;**ortak**&gt;**ürünleri piyasaya**.
2.  Ürünü seçin ve ardından **Ürün boyutları**'na tıklayın.
3.  Ürün boyutları için bağlantılardan birini seçin: **Yapılandırmalar**, **Boyutlar**, **Renkler** veya **Stil**.
4.  Boyut değerini seçin ve ardından **Çevir**'e tıklayın.
5.  **Metin çevirisi** sayfasında **Dil** alanında, bir dil seçin. Daha fazla dil eklemek için Genişlet **dil** alan ve'ı **Tamam**.
6.  İçinde **çevrilmiş metni** grup, çeviri girin **adı** ve **açıklama** alanlar.

## <a name="can-the-names-of-product-variants-be-translated"></a>Ürün çeşitlerinin adları çevrilebilir mi?
Ürün çeşitleri, serbest bırakılan bir ürünün boyutlarına bağlıdır. Ürün çeşitleri adları boyut değerlerinin bir birleşimine bağlıdır. Ürün çeşidiyle ilişkilendirilen boyut değerleri çevrildiğinde, ürün çeşidinin adı çevrilmiş sürümde görünür.  

**Example**  

Ürününüz farklı boyut ve renklerde bir Tişörttür ve çeşit adları aşağıdaki ayrıntılara bağlıdır:
-   Ürün numarası: \#3
-   Boyutlar: Boyut ve renk
-   Boyut değerleri: Küçük, Orta, Büyük
-   Renk boyut değerleri: Kırmızı, Yeşil, Siyah

Boyut üzerinde temel bir ürün değişken adını küçük değerler ve kırmızı **\#3:Small:Red**.  

Müşteri birkaç tane küçük, kırmızı tişört satın almak istiyorsa, Tişört adı fatura üzerinde Türkçe olarak görünmelidir. Boyut değerlerini, küçük ve kırmızı, Fransızcaya çevirebilir ve ürün değişken adı **\#3: Petit: Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tip</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Müşterinin tercih ettiği dili ayarlamak için aşağıdaki adımları izleyin:
<ol>  
<li>' I <strong>satış ve pazarlama</strong>&gt;<strong>ortak</strong>&gt;<strong>müşteriler</strong>&gt;<strong>tüm</strong> <strong>müşteriler</strong>.</li>
<li><strong>Müşteriler</strong> sayfasını açmak için bir müşteriye çift tıklayın. <strong>Genel</strong> sekmesinde <strong>Dil</strong> alanında <strong>dili</strong> seçin.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Müşterinin tercih ettiği dil için kullanılabilir bir çeviri mevcut değilse ne olur?
Çeviriler müşterinin tercih ettiği dilde kullanılabilir değilse adlar ve açıklamalar şirketinizin küresel dilinde görüntülenir.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Aynı anda bir dizi boyut değerinin çevirilerini yönetebilir miyim?
Boyut değerleri ürüne özeldir ve her ürün için boyut değerleri çevirilerini yönetebilirsiniz. Ancak bir boyut değeri grubu ve değer grubundaki değerler için çeviriler oluşturursanız çevirileri yönetmek daha kolay olur.   

**Example**  

Şirketiniz farklı stillerde Tişörtler üretir ve her stilin Küçük, Orta ve Büyük boyutları bulunur. Boyutlar, bir boyut değeri grubunda toplanır. Yeni bir Tişört stili eklendiğinde bu stili boyutlar için kullanılan boyut değeri grubuyla ilişkilendirebilirsiniz; böylece ürünün tüm boyutları kullanılabilir. Ayrıca istediğiniz zaman boyut değeri grubundaki boyutlar için çeviriler ekleyebilir veya çevirileri değiştirebilirsiniz.  

Boyut çeşidi grubu aracılığıyla bir ürünle ilişkilendirilen boyut değeri ürün çeşidi grubunda saklanmalıdır.   
Boyut değeri grubu oluşturmak için aşağıdaki adımları izleyin:
1.  ' I **ürün bilgi yönetimi**&gt;**Kurulum**&gt;**değişken grupları**.
2.  **Boyut** **grupları**, **Renk grupları** veya **Stil grupları**'nı seçin.
3.  ' I **yeni**ve sonra grubu için bir ad girin **boyutu****grup**, **renk grubu**, veya **Stil grubu** alan. Gruplar için satırlar oluşturmak için **Boyutlar**, **Renkler** veya **Stiller**'e tıklayın.
4.  İçinde **boyutu****grup** satırları **renk****grup****satırları**, veya **Stil grubu satırları** sayfa, tıklatın **yeni**ve boyutları, renkleri ve stilleri gruplar oluşturun.

Boyut değeri grubundaki değerler için çevirileri yönetmek üzere aşağıdaki adımları izleyin:
1.  **Ebat grubu satırları**, **Renk grubu satırları** veya **Stil grubu satırları** sayfasını açmak için bir boyut değeri grubu oluşturmak üzere önceki yordamdaki adımları izleyin.
2.  **Metin çevirisi**'ne tıklayın. İçinde **metin çeviri** sayfa içinde **çevrilmiş metni** grup, çeviri girin **adı** ve **açıklama** alanlar.

## <a name="when-can-translations-of-productrelated-information-be-managed"></a>Ne zaman productrelated bilgi çevirilerini yönetilebilir?
Ürünle ilgili bilgilerin çevirileri her an yönetilebilir. Çeviriler bir ürünle ilişkilendirilmiş bir boyut değeri için güncelleştirildiğinde, ürünün hareketlere sahip olmasına bakılmaksızın ürün bilgileri güncelleştirilir.




