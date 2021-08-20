---
title: Tahsisat koşulları
description: Bu konu, bir ana hesapta tahsisat koşullarının kullanılması hakkında bilgi sağlar.
author: rachel-profitt
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount, AllocationTerms
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-06-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 957baba1364fbbd4a51c6f51b0fad5bf8db46680fa97b9d3d0474dc015064609
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776540"
---
# <a name="allocation-terms"></a>Tahsisat koşulları

[!include [banner](../includes/banner.md)]

Bu konu, bir ana hesapta tahsisat koşullarının kullanılması hakkında bilgi sağlar. Tahsisat koşulları, tutarları birden fazla genel muhasebe hesabı birleşimleri arasında dağıtmak için kullanılır. Gelir ve giderlerin muhasebede doğru nesneye yazılmasını sağlamaya yardımcı olurlar.

Ana hesapta oluşturduğunuz her tahsisat koşulu, tek kaynaklı bir ana hesaptan ve mali boyutların bir bileşiminden tahsis edilecek fişin yüzdesini tanımlar. Ek olarak, hedef ana hesabı ve tutarın tahsis edileceği mali boyutları siz tanımlarsınız. 

Tahsisat için kaynak mali boyut tanımladığınızda, her boyutun belirli mi yoksa özel mi olduğunu seçebilirsiniz. Özel, kaynak hareketin mali boyutunun seçili boyutla eşleşmesi gerektiğini belirtir. Belirsizi seçtiğinizde, mali boyutun herhangi bir değeri bir eşleşmeye katkıda bulunabileceğini gösterir.

Bir tahsisat koşuluyla ilgili olarak hedef genel muhasebe hesabını tanımladığınızda, tutarı tahsis ettiğiniz ana hesabı belirtmeniz gerekir. Kaynak hareketin deftere nakledildiği ana hesabı veya farklı bir ana hesabı kullanabilirsiniz. Aynı ana hesap kullanılırsa, kayıt kaydedilirken bir uyarı görüntülenir. Ana hesabı belirtmenin yanı sıra, hedef boyutları da belirtmeniz gerekir. Her boyut için kaynak mali boyut değerini korumak veya değiştirmek istediğinizi belirtebilirsiniz. Hayır'ı seçerseniz, mali boyut için yeni bir değer seçmeniz gerekir. Evet'i seçerseniz, ek bilgi belirtilmez ve deftere nakil yaptığınızda sistem özgün mali boyutları korur.

Bir ana hesaba ekleyebileceğiniz tahsisat koşulları sayısı için bir sınır yoktur; ancak, bir tahsisat teriminde tahsis edilecek yüzde toplamı 100'ü geçemez. Orijinal fiş tutarının bir kısmının kaynak mali boyutlarında kalması gerekiyorsa, yüzde 100'den az tahsisat oluşturabilirsiniz. Tahsisat koşulları, tüzel kişilik geçersiz kılma olarak ana hesaba eklenebilir. Paylaşılan bir hesap planı kullanıyorsanız, tahsisat koşullarının her tüzel kişilik için tanımlanması gerekir. **Tahsisat koşulları** düğmesine erişmek için önce Tüzel kişilik geçersiz kılmada **Tahsisat** onay kutusunu seçmeniz gerekir.

## <a name="allocation-term-example"></a>Tahsisat koşulu örneği
Kuruluşunuz için 000 olarak numaralandırılmış CORPORATE adında bir maliyet merkezi tanımladınız. Faturalar tesis giderleri için deftere nakledildiğinde, bunlar CORPORATE maliyet merkezine kodlanır. Şirketiniz tüm tesis giderlerinin her maliyet merkezi için bir yüzdeye göre tahsis edileceği bir kural tanımladı. Bölüm ve iş birimi ile ilgili diğer mali boyutlar aynı kalır.

Bu örnekte, tesis gideri ana hesabı için yeni bir tahsisat koşulu oluşturulur. Her maliyet merkezi için tahsis edilecek yüzdeyle bir satır oluşturulur. Her satırın kaynak mali boyutları için **Seçim ölçütü** **Maliyet merkezine** **Özeldir** ve değer 000 olarak ayarlanır: CORPORATE. Bölüm ve iş birimi için **Seçim ölçütü** **Belirsiz** olacaktır.

**Hedef kayıt defter, hesabı** hızlı sekmesinde, ana hesap aynı tesis gideri hesabı olur ve **Kaynak mali boyutları koru**, **İş birimi** ve **Bölüm** için **Evet** olarak ayarlanır. **Kaynak mali boyutları koru**, **Maliyet merkezi** için **Hayır** olarak ayarlanır ve seçilen değer, tahsis ettiğiniz her maliyet merkezi olur. Tahsis edilecek üç maliyet merkezi varsa, üç tahsisat koşulu kaydı oluşturulur. Her tahsisat koşulu arasındaki tek fark, hedef kayıt defterinde belirtilen maliyet merkezidir.

## <a name="create-an-allocation-term-on-a-main-account"></a>Ana hesapta tahsisat koşulu oluşturma

1. **Gezinti bölmesinde** **Modüller > Genel kayıt defteri > Hesap planı > Hesaplar > Ana hesaplar**'a gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. **Tüzel kişilik geçersiz kılmaları** hızlı sekmesinde **Ekle**'yi seçin.
4. **Şirket**'i ve **Ekle**'yi seçin.
5. **Tahsisat** onay kutusunu işaretleyin.
6. **Tahsisat koşulları**'nı seçin.
7. Varsayılan kaydı değiştirmek için **Düzenle**'yş seçin veya bir kayıt eklemek için **Yeni**'yi seçin.
8. **Yüzde** alanına, tahsis etmek istediğiniz fiş hareketlerinin yüzdesini girin.
9. **Kaynak finansal boyut** hızlı sekmesinde, her mali boyutla ilgili **Seçim ölçütleri** için bir seçenek belirleyin.
    - **Özel**'i seçerseniz, sağdaki açılan kutuda mali boyut değerini seçin.
    - **Belirsiz** seçeneğini belirlerseniz mali boyut için ek bilgi gerekmez.
10. **Hedef kayıt defteri** hesabı hızlı sekmesinde **Hedef hesap** alanında, fiş hareketinin yüzdesini tahsis etmek istediğiniz ana hesabı seçin.
11. Her mali boyut için **Kaynak mali boyutlarını koru** alanında bir seçenek belirleyin.
    - **Hayır**'ı seçerseniz, sağda açılan kutuda fiş hareketinin tahsis edilmesini istediğiniz mali boyut değerini seçin.
    - **Evet**'i seçerseniz, ek bilgi gerekmez. Sistem, tahsisatı deftere naklederken özgün fişteki değeri koruyacaktır.
12. Her ek tahsisat için 7-11 arasındaki adımları yineleyin. Tüm tahsisatların toplamı **Toplam yüzde** alanında belirtilir. Bu tutar 100'ü geçemez.
13. Tüm sayfaları kapatın.

>[!NOTE] 
> Seçili tahsisatı çoğaltmak için isteğe bağlı olarak **Kopyala** düğmesini de kullanabilirsiniz.

Bir ana hesap için tahsisat koşulu oluşturulduğunda, tahsisat koşullarında kaynak mali boyutlarla eşleşen bir fiş nakledildiğinde, sistem otomatik olarak yeni bir fiş nakleder.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]