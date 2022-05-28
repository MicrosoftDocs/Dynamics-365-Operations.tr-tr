---
title: Müşteriler için kredi yönetimi bilgileri ekleme
description: Bu konu, müşteri için kredi yönetimi bilgilerinin nasıl eklendiğini açıklamaktadır.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d5ced2f2bc419f18431663273236d21546c5541b
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734471"
---
# <a name="add-credit-management-information-for-customers"></a>Müşteriler için kredi yönetimi bilgileri ekleme

[!include [banner](../includes/banner.md)]

Kredi yönetimini denetleyen parametreleri ayarladıktan sonra, her bir müşteri için daha fazla ayrıntı ekleyebilirsiniz. Bu ayrıntılar kredi yönetimi işlemlerini kontrol eder ve ayrıca tahsilat ekibi üyelerinin müşterileri yönetmesine yardımcı olacak ek bilgiler de sağlar.

## <a name="customer-information"></a>Müşteri bilgileri

Müşteri ayrıntılarını **Tüm müşteriler** sayfasının (**Alacak hesabı \> Müşteriler \> Tüm müşteriler**) **Alacak ve tahsilatlar** hızlı sekmesinde ekleyebilirsiniz.

1. Müşterinin herhangi bir kredi limiti testiyle sınırlanmaması gerekiyorsa **Sınırsız kredi limiti** seçeneğini **Evet** olarak ayarlayın.
2. Müşteriyi genellikle kredi yönetimi işlemleri sırasında oluşan herhangi bir eylemin dışında tutmak için **Kredi yönetiminden hariç tut** seçeneğini **Evet** olarak ayarlayın.
3. Müşteri için kredi yönetimi grubunu seçin.
4. Kredi limitini müşterinin para biriminde hesaplamak için, **Müşterinin para birimi cinsinden kredi limiti** alanına müşterinin kredi limitini girin. Şirket para birimi cinsinden kredi limiti, **Kredi yönetimi parametreleri**'nde seçilen kredi limiti döviz kuru türüyle tanımlanan döviz kurlarıyla dönüştürülür.
5. **Son inceleme tarihi** alanına, müşterinin kredi limitinin bir kredi yöneticisi tarafından en son incelendiği tarihi girin.
6. **Zamanlanan sonraki inceleme tarihi** alanına, müşteri için belirlenen kredi inceleme ve güncelleştirme zamanının tarihini.
7. **Uygun kredi limiti** alanına, müşterinin kredi geçmişinin incelenmesine dayanarak, müşteriye atanabilecek en yüksek kredi limitini girin. Uygun kredi limiti, **Alacak ve koleksiyonlar** hızlı sekmesinde gösterilen kredi limitinden farklı olabilir.
8. **Uygun kredi limiti para birimi** alanına, uygun kredi limitinin para birimini girin.
9. **Uygun kredi limiti tarihi** alanına, uygun kredi limitinin oluşturulduğu tarihi girin.
10. **Kredi hesabı durumu** alanına, müşterinin kredi hesabı durumunu girin.
11. **Durum nedeni** alanına, hesap durumuyla ilişkili nedeni girin.
12. Müşterinin şu anda bir kredi acentesine atandığını belirtmek için, **Acenteyle** seçeneğini **Evet** olarak ayarlayın. Bu değer yalnızca bilgi amaçlıdır. Kredi yönetimi işlemlerinde kullanılmaz.
13. Şirkete ilişkin bir unvan kullanıldığını göstermek için, **Kullanılan unvan** seçeneğini **Evet** olarak ayarlayın. Bu değer yalnızca bilgi amaçlıdır. Kredi yönetimi işlemlerinde kullanılmaz.
14. **İş başlangıç tarihi** alanına, müşterinin işe ilk başladığı tarihi girin. Bu bilgiler risk puanları oluşturulurken kullanılır.
15. **Müşterilik başlangıç tarihi** alanına, müşteri için ilk hareketlerin işlendiği tarihi girin. Bu bilgiler risk puanları oluşturulurken kullanılır.
16. Müşterinin kredi tutarını daha fazla değerlendirmek için kredi ekibinin kullanabileceği notlar girin.

> [!Note] 
> **Müşteri** sayfasında gösterilen bazı bilgiler başka bir işlem tarafından oluşturulmuştur:

- **Kredi limiti bitiş tarihi** alanı, kredi limitinin sona ereceği tarihi gösterir. Bu alanı ayarlamazsanız, müşterinin kredi limiti sona ermez.
- **Kredi limiti tarihi** alanı, kredi limitinin oluşturulduğu tarihi gösterir. Kredi limiti her ayarlandığında bu alan güncelleştirilir.
- Geçici kredi limitleri, bir döneme ait müşteri kredi limitini geçersiz kılar. Bunlar, toplam kredi limitini hesaplamak için kredi limiti yerine kullanılır. Bu bilgiler yalnızca etkin bir kredi limiti varsa gösterilir. Kredi limiti ayarlamalarını kullanarak geçici kredi limitleri ekleyebilirsiniz.
- **Sigorta ve garantiler** alanı, müşteri için kredi limitini artırabilecek sigorta ve garantilerin toplam değerini gösterir.
- **Toplam kredi limiti** alanı, müşteriye ilişkin nihai kredi limitini gösterir. Toplam kredi limiti, sigorta ve garantileri ve geçici kredi limitlerini içerir.

## <a name="temporary-credit-limits"></a>Geçici alacak limitleri

Geçici kredi limitleri, belirli bir döneme ait müşteri kredi limitlerini geçersiz kılar. Kredi limiti ayarlamalarını kullanarak geçici kredi limitleri ekleyebilirsiniz. Kredi limiti ayarlamaları, kredi yöneticilerinin bir deftere nakil işlemiyle tek bir müşterinin, bir müşteri grubunun veya tüm müşterilerin kredi limitlerini ve kredi bitiş tarihlerini güncelleştirmelerini sağlar.

**Kredi limiti ayarlamaları** sayfasında (**Kredi yönetimi \> Kredi limiti ayarlamaları \> Kredi limiti ayarlamaları**) kredi limiti ayarlama girişleri oluşturabilirsiniz.

## <a name="create-insurance-policies-and-guarantees"></a>Sigorta poliçeleri ve garantiler oluşturma

Her müşteri için bir veya daha fazla sigorta poliçesi ve garanti oluşturabilirsiniz. Bunun ardından, şirketinizin müşteriye kredi sunduğu kapsamı hesaplamak için bunları kullanabilirsiniz. Sigorta poliçeleri ve garantiler de bir müşteri için kredi limitine dahil edilebilir.

**Tüm müşteriler** sayfasında (**Alacak hesapları \> Müşteriler \> Tüm müşteriler**) sigorta poliçeleri ve garantiler oluşturabilirsiniz. Bir müşteri seçin ve ardından eylem bölmesinde, **Müşteri** sekmesinde **Sigorta ve garantiler**'i seçin.

> [!NOTE]
> Aşağıdaki yordamda, genel adres defterinden bir sigortacı veya kefil seçeceksiniz. Bu nedenle, bu yordama başlamadan önce, sigortacıların ve kefillerin genel adres defterine eklenmiş olduğundan emin olmalısınız.

1. **Kimlik tanımlayıcı** alanına **Garanti** veya **Sigorta** girin.
2. **Garanti/Sigorta türü** alanında, daha önce ayarlamış olduğunuz garanti veya sigorta türlerinden birini seçin.
3. **Sigortacı/Kefil** alanında, genel adres defterinden sigortacıyı veya kefili seçin. 
4. **Kimlik tanımlayıcı** alanında **Sigorta**'yı seçtiyseniz, **Poliçe kapsamı türü** alanında, daha önce ayarlamış olduğunuz kapsam türlerinden birini seçin. Garanti için bir poliçe kapsamı türü seçemezsiniz.
5. **Kimlik** alanına, poliçenin kodunu girin. Bu kod genellikle bir poliçe numarasıdır.
6. **Yürürlüğe giriş** alanına, sigorta poliçesinin veya garantinin başlangıç tarihini girin.
7. **Bitiş tarihi** alanına, sigorta poliçesinin veya garantinin bitiş tarihini  girin.
8. **Değer** alanına, sigorta poliçesinin veya garantinin değerini girin. Bu değer, poliçenin tam değeridir.
9. **Para birimi** alanında, poliçe değerinin para birimini seçin. 
10. **Kredi limitini güncelleştir** alanında, **0** ile **100** arasında bir yüzde değeri belirtin. Bu yüzde değeri poliçe değerine uygulanır ve elde edilen sonuç, kredi limiti hesaplamalarında kullanılan kredi limitini artırmak için kullanılır. Hesaplanan değer, **Müşteriler** sayfasının **Alacak ve tahsilatlar** hızlı sekmesindeki **Toplam kredi limiti, Sigorta ve Garantiler** altında gösterilir.

    Aşağıda bir örnek verilmiştir:

    - Kredi limiti (A) 100.000.
    - Poliçe değeri (B) 50.000.
    - **Kredi limitini güncelleştir** yüzdesi (C) 50,00.
    
    Bu durumda, yürürlükteki kredi limiti 125.000 (= A + \[B × C\]) olur.

11. Kredi limiti hesaplamalarında kullanılan kredi limitinden poliçenin tam değerini düşmek için **Kapsama dahil** onay kutusunu işaretleyin. Bu onay kutusu işaretlenirse, **Kredi limitini güncelleştir** yüzdesi belirtildiğinde hesaplanan değer, kredi limiti hesaplamalarında kullanılmaz.

    Aşağıda bir örnek verilmiştir:

    - Kredi limiti (A) 100.000.
    - Poliçe değeri (B) 50.000.
    - **Kredi limitini güncelleştir** yüzdesi (C) 50,00.

    Bu durumda, yürürlükteki kredi limiti 125.000 (= A + \[B × C\]) olur.
    
    Ancak , **Kapsama dahil** onay kutusunu işaretlerseniz, 50.000 (=100.000'in %50'si) olan **Kredi limitini güncelleştir** değeri kaldırılır ve kapsam değeri 75.000 (= A + \[B × C\] – B) olur.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
