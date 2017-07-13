---
title: Adres defterleri
description: 
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 7b3bed2bec4b109c6e3b557b8c3651f15f25169c
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017


---

# <a name="address-books"></a>Adres defterleri

[!include[banner](../includes/banner.md)]




<a name="how-do-i-check-for-duplicate-records"></a>Tekrarlanan kayıtları nasıl denetlerim?
-------------------------------------

Yinelenen kayıtları doğrudan **genel adres defteri** listesi sayfasından denetleyebilirsiniz. Eylem bölmesinde, **Taraf** sekmesinde, **Sürdür** grubunda, **Tekrarlananları denetle**'ye tıklayın. Sonra tekrarlananları denetlemeye dahil edilecek değerleri seçin.

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Bir adres defterine taraf kayıtlarını toplu ekleyebilir veya silebilir miyim?
Evet, bir adres defterine çok sayıda taraf kaydını ekleyebilir ve ayrıca çok sayıda taraf kaydını silebilirsiniz.

-   Birden fazla taraf kaydını bir adres defterine eklemek için **Genel adres defteri** liste sayfasında, tarafları listeden seçin. Sonra eylem bölmesinde, **Taraf** sekmesinde, **Sürdür** grubunda, **Taraf ata**'ya tıklayın. Taraf kayıtlarının ekleneceği adres defterini seçin ve sonra **Tamam**'a tıklayın. Seçilen tüm taraf kayıtları, seçmiş olduğunuz adres defterlerine eklenecektir.
-   Birden fazla taraf kaydını bir adres defterinden silmek için **Genel adres defteri** liste sayfasında, tarafları listeden seçin. Sonra eylem bölmesinde, **Taraf** sekmesinde, **Sürdür** grubunda, **Taraf sil**'e tıklayın. Tarafların kaldırılacağı adres defterlerini seçin ve sonra **Tamam**'a tıklayın. Seçilen tüm taraf kayıtları, seçmiş olduğunuz adres defterlerinden silinecektir.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Bir kaydın taraf türünü değiştirebilir miyim yoksa kaydı silip yeni bir tane oluşturmam mı gerekir?
Bazen bir kaydın taraf türünü kişiden kuruluşa ya da kuruluştan kişiye değiştirmeniz gerekebilmektedir. Örneğin Nancy Fabrikam İngiltere için satış ekibinin bir üyesidir. Londra'daki ticaret fuarında altı yeni ada müşteri ile tanışır. Nancy her aday için bir aday taraf kaydı oluşturur. Nancy kayıtları kaydettiğinde, her kayıt genel adres defterinde de oluşturulur. Fabrikam, varsayılan taraf türünü kuruluş olarak ayarlamıştır fakat yeni adayların ikisinin kayıt türü kişi olmalıdır. Bu nedenle, Nancy fuardan geri döndüğünde, iki adayın taraf türünün kayıtlarını değiştirmesi gerekir. Bir taraf kaydını bir taraf türünden diğerine değiştirmek için önce genel adres defteri içinde doğru türde yeni bir taraf kaydı oluşturmalısınız. Eski taraf kaydını daha sonra bu yeni kayıtla ilişkilendirin. Yeni taraf ilişkilendirmesini yaptıktan sonra, yanlış kayıt türüne sahip olan özgün taraf kaydını silin.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>Bir taraf kaydının adını veya adresini nasıl değiştirebilirim?
Bir taraf kaydının adını veya bu kayıtla ilişkili adresleri istediğiniz anda güncelleştirebilirsiniz.

-   Taraf kaydının adını güncelleştirmek için parti kaydını açın ve sonra eylem bölmesinde **Düzenle**'ye tıklayın. **Genel** hızlı sekmesi üzeirnde taraf için yeni bir ad girin ve sonra kaydı kaydedin.
-   Bir taraf kaydının adresini güncelleştirmek için taraf kaydını açın ve daha sonra **Adresler** hızlı sekmesinde güncelleştirilecek adresi seçin. **Düzenle**'ye tıklayın ve daha sonra **Adresi düzenle** sayfasında, adres veya adres parametrelerinde gerekli değişiklikleri yapın.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>İki veya daha fazla taraf kaydını tek bir kayıtta birleştirebilir miyim?
Bazen, bir ya da daha fazla taraf kaydını tek bir kayıtta birleştirmek isteyebilirsiniz. Bir ya da birden fazla yinelenen taraf kaydını kasıtlı veya kasıtsız olarak oluşturursanız bu durum ortaya çıkabilir. Taraf kayıtlarını birleştirdiğinizde, tutmak için bir kayıt seçin. Diğer kayıtların bilgileri daha sonra bu kayıtta birleştirilecektir. Örneğin, Fabrikam hakkında bilginin üç taraf kaydında depolandığını fark edersiniz: A, B ve C. Taraf kaydı A'yı tutmaya karar verirsiniz. Bu nedenle, B ve C taraf kayıtlarında depolanan bilgileri taraf kaydı A'da birleştirilir. Taraf kayıtlarını birleştiremeyeceğiniz bazı durumlar da mevcuttur:

-   Müşteri veya satıcı gibi aynı taraf rolüyle aynı tüzel kişilikte ilişkilendirilmiş olan taraf kayıtlarını birleştiremezsiniz. Örneğin, taraf A tüzel kişilik 123'teki bir müşteriyle ilişkilendirilir ve taraf B tarafı tüzel kişilik 123'teki başka bir müşteriyle ilişkilendirilir. Bu taraf kayıtları birleştirilemez, çünkü birleştirilmeleri durumunda, birleştirilen taraf kaydının aynı tüzel kişilik içinde birden çok müşteriyle ilişkilendirilmesi gerekir ve bu izin verilmez. Ancak kayıtlar taraf B tüzel kişilik 123'deki bir satıcı veya başka bir tüzel kişilikteki bir müşteri ile ilişkilendirilirse birleştirilebilirler.
-   Aynı tüzel kişilikteki, takımdaki veya işletme birimindeki dahili taraf kuruluş kayıtlarını birleştiremezsiniz.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Genel Adres Defteri'nde mi yoksa Müşteri veya Satıcı sayfası gibi bir başka yerde mi taraf kaydını oluşturmalıyım?
Taraf kayıtlarını Genel Adres Defteri'ne veya uygun varlık sayfasında girebilirsiniz. Bir konuma bir kayıt eklediğinizde, aynı kayıt her zaman diğer konuma eklenir. Örneğin, bir müşteri için taraf kaydını genel adres defterine eklerseniz, kayıt **Müşteri** sayfasına da eklenir. Benzer şekilde, bir müşteri için taraf kaydını **Müşteri** sayfasına eklerseniz, kayıt genel adres defterine de eklenir. Yeni taraf kayıtlarını nereye gireceğinize karar vermek için aşağıdaki yönergeleri kullanın:

-   **Varlık türünü bilmiyorken bir taraf kaydı oluşturmak** – Eğer bir taraf kaydı oluşturmanız gerekiyor fakat varlık türünü bilmiyorsanız (örneğin, varlığın bir müşteri mi yoksa fırsat mı olduğunu), kaydı genel adres defterinde oluşturun. Varlık türünü daha sonra seçebilirsiniz.
-   **Varlık türünü biliyorken bir taraf kaydı oluşturmak** – Tarafın varlık türünü biliyorsanız, kaydı bu türe uygulanabilir sayfada oluşturabilirsiniz. Örneğin bir müşteri için kaydı **Müşteri** sayfasında oluşturun. Bir kaydı varlığa uygun sayfada oluşturur ve kaydederseniz, kayıt otomatik olarak genel adres defterinde oluşturulacaktır.

## <a name="can-i-translate-address-information-for-party-records"></a>Taraf kayıtları için adres bilgilerini çevirebilir miyim?
Adres bilgilerinin çevirilerini ayarlayabilirsiniz, böylece bilgiler Microsoft Dynamics 365 for Finance and Operations içerisinde kullanıcı dilinde (sistem dili) görüntülenirken, satış siparişleri gibi belgelerde farklı bir dilde görüntülenecektir. Ülke/bölge adları, adres amaçları ve isim serileri için çeviriler girebilirsiniz. Örneğin, sistem dilinizi Danca'dır ve Fransa'daki bir müşteri için bir satış siparişi oluşturursunuz. Bu durumda, müşteri kaydını program içerisinde Danca olarak görüntüleyebilir fakat yazdırılan satış siparişinde adres bilgilerini Fransızca görüntüleyebilirsiniz. Çevirileri ayarladığınızda, listedeki her öğe için çeviri girmeniz gerekir. Çeviri girmediğiniz her öğe sistem dilinde görüntülenecektir. Örneğin, sistem dilinizi Danca'dır ve İspanya'daki bir müşteriye bir belge gönderiyorsunuz. Adres bilgileri için İspanyolca (ESP) çeviriler girmediyseniz, bu bilgiler hem programda hem de yazdırılan belgede Danca olarak görünür.




