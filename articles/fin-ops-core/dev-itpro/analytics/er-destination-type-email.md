---
title: E-posta ER hedef türü
description: Bu konuda, Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için e-posta hedefinin nasıl yapılandırılacağı açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e2e0da1c724269e0956be2f402b34ff376ed1990
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094116"
---
# <a name="email-er-destination-type"></a>E-posta ER hedef türü

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) biçimi çalıştırıldığında, bir veya daha fazla giden belge oluşturulabilir. **Klasör** veya **Dosya** biçimi bileşenleri, giden belgelerin yapısını belirtmek amacıyla ER biçimlerinde kullanılır. Giden belgeleri e-posta eki olarak göndermek üzere bu bileşen türleri için bir e-posta hedefi yapılandırabilirsiniz.

Bir ER biçiminin her **Klasör** veya **Dosya** bileşeni için bir e-posta hedefi yapılandırabilirsiniz. Bu durumda, **her giden belge ayrı bir e-postayla gönderilir**. Bu hedef ayarına bağlı olarak, oluşturulan bir belge e-posta eki olarak teslim edilir. 

> [!NOTE]
> İlgili **Dosya** bileşeni için **Etkin** ifadesi **False** Boole değeri döndürecek şekilde yapılandırıldığından belge üretilmezse, bileşen için e-posta hedefi yapılandırılmış ve etkinleştirilmiş olsa bile, e-posta gönderilmez.

Ayrıca, birden fazla **Klasör** veya **Dosya** bileşenini bir arada [gruplandırabilir](#grouping) ve ardından gruptaki tüm bileşenler için bir e-posta hedefi yapılandırabilirsiniz. Bu durumda, gruba ait bileşenler tarafından oluşturulan tüm giden belgeler **tek bir e-postanın birden çok eki olarak gönderilir**. Bu hedef ayarına bağlı olarak, oluşturulan her bir belge tek bir e-postanın eki olarak teslim edilir.

> [!NOTE]
> Bileşen grubundaki bir **Dosya** bileşeni tarafından en az bir belge oluşturulursa bir e-posta gönderilir. Her bir ilgili **Dosya** bileşeni için **Etkin** ifadesi **False** Boole değeri döndürecek şekilde yapılandırıldığından gruplandırılmış bileşenler belge üretmezse, bileşen grubu için e-posta hedefi yapılandırılmış ve etkinleştirilmiş olsa bile, e-posta gönderilmez.
>
> **E-posta**, bir bileşen grubu için yapılandırılabilecek tek hedeftir. Bir grubun e-posta hedefi ayarına bağlı olarak e-postayla gönderilmiş bir belgeyi teslim etmek için, bir hedef kaydı daha ekleyin, istediğiniz bileşeni seçin ve ardından bu kayıt için başka bir hedef yapılandırın.

Tek bir ER biçimi yapılandırması için birden çok bileşen grubu yapılandırılabilir. Bu şekilde, her bileşen grubu için bir e-posta hedefi ve tüm bileşenler için bir e-posta hedefi yapılandırabilirsiniz.

## <a name="configure-an-email-destination"></a>E-posta hedefi yapılandırma

Bir veya birden fazla çıkış dosyasını e-postayla göndermek için **Elektronik raporlama hedefi** sayfasındaki **Dosya hedefi** hızlı sekmesinde ızgaradan bir bileşen veya bileşen grubu seçin ve ardından **Ayarlar**'ı seçin. Gösterilen **Hedef ayarları** iletişim kutusundaki **E-posta** sekmesinde **Etkin** seçeneğini **Evet** olarak ayarlayın. Ardından e-posta alıcılarını belirtebilir ve e-posta iletisinin konusunu ve metnini düzenleyebilirsiniz. E-posta metni ve konusu için sabit bir metin ayarlayabilir veya ER [formüllerini](er-formula-language.md) kullanarak dinamik e-posta metinleri oluşturabilirsiniz.

E-posta adreslerini ER içerisinde iki şekilde yapılandırabilirsiniz. Yapılandırma, aynen Yazdırma Yönetimi özelliğinin tamamladığı şekilde tamamlanabilir veya bir formülle bir e-posta yapılandırmasına doğrudan başvuru kullanarak bir e-posta adresini çözümleyebilirsiniz.

[![E-posta hedefi için Etkin seçeneğini Evet olarak ayarlama](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>E-posta adresi türleri

**Hedef ayarları** iletişim kutusundaki **Kime** veya **Bilgi** alanının yanındaki **Düzenle**'yi seçerseniz **E-posta gönderilecek adres** iletişim kutusu gösterilir. **Ekle**'yi seçin ve ardından kullanılacak e-posta adresinin türünü seçin. Şu anda **Yazdırma Yönetimi e-postası** ve **Yapılandırma e-postası** olmak üzere iki tür e-posta desteklenmektedir.

[![E-posta adresinin türünü seçme](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Yazdırma Yönetimi e-postası

E-posta adresi türü olarak **Yazdırma Yönetimi e-postası**'nı seçerseniz aşağıdaki alanları ayarlayarak **E-posta gönderilecek kişi** iletişim kutusuna sabit e-posta adresleri girebilirsiniz:

- **E-posta kaynağı** alanında **Hiçbiri** seçeneğini belirleyin.
- **";" ile ayrılan ek e-posta adresleri** alanına sabit e-posta adreslerini girin.

Alternatif olarak, giden belge oluşturduğunuz tarafın ilgili kişi ayrıntılarının içinden de e-posta adresleri edinebilirsiniz. Sabit olmayan e-posta adreslerini kullanmak için **E-posta kaynağı** alanında dosya hedefi için tarafın [rolünü](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles) seçin. Aşağıdaki roller desteklenir:

- Müşteri
- Satıcı
- Aday müşteri
- Başvur
- Rakip
- Çalışan
- Başvuran
- Olası satıcı
- Onaylanmamış satıcı

Örneğin, satıcı ödemelerini işlemek amacıyla kullanılan bir ER biçimi için e-posta hedefi yapılandırırken **Satıcı** rolünü seçin.

İstenen rolü seçtikten sonra, [Formül tasarımcısı](general-electronic-reporting-formula-designer.md) sayfasını açmak için **E-posta kaynak hesabı** alanının yanındaki **Bağla** düğmesini (zincir simgesi) seçin. Ardından, işlenen belgeden e-posta hedefine yapılandırılan role atanan tarafın hesap numarasını çalışma zamanında döndüren formülü yapılandırmak için bu sayfayı kullanabilirsiniz.

> [!NOTE]
> Formüller ER yapılandırmasına özgüdür.

**Formül tasarımcısı** sayfasında, **Formül** alanına, desteklenen bir role belgeye özel bir referans girin. Referansı yazmak yerine, **Veri kaynağı** bölmesinde, yapılandırılan rolün hesabını temsil eden veri kaynağı düğümünü seçin ve ardından formülü güncelleştirmek için **Veri kaynağı ekle**'yi seçin. Örneğin, satıcı ödemelerini işlemek için kullanılan **ISO 20022 Borç Transferi** yapılandırması ile ilgili e-posta hedefini yapılandırıyorsanız satıcı hesabını temsil eden düğüm `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID` öğesidir.

![Bir e-posta kaynağı hesabını yapılandırma](./media/er_destinations-emaildefineaddresssource.gif)

Yapılandırılan rolün hesap numaraları Microsoft Dynamics 365 Finance'in tüm kurulumu için benzersiz ise **E-posta gönderilecek adres** iletişim kutusundaki **E-posta kaynağının şirketi** alanı boş kalabilir.

Bunun yerine, [Genel adres defteri](../../fin-ops/organization-administration/overview-global-address-book.md)'ndeki farklı tarafların yapılandırılan rolü doldurmak için hepsinin aynı hesap numarasını kullanacağı şekilde farklı şirketlerde ([tüzel kişilikler](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)) kaydedildiği bir durumla karşılaşabilirsiniz. Bu durumda, yapılandırılan rolün hesap numaraları tüm Finance kurulumu için benzersiz değildir. Bu nedenle, bir tarafı açıkça seçmek için yalnızca hesap numarası belirtmeniz yeterli değildir. Ayrıca yapılandırılan rolü doldurmak için tarafın kaydedilği şirketi de belirtmeniz gerekir. [Formül tasarımcısı](general-electronic-reporting-formula-designer.md) sayfasını açmak için **E-posta gönderilecek adres** iletişim kutusundaki **E-posta kaynağının şirketi** alanının yanındaki **Bağla** düğmesini (zincir simgesi) seçin. Ardından, kapsamında istenen kaynağın bulunması gereken şirket kodunu çalışma zamanında döndüren formülü yapılandırmak için bu sayfayı kullanabilirsiniz.

> [!TIP]
> Bir ER biçimini çalıştırmak için şirket kodunu kullanmanız gerekiyorsa ancak ER biçimi şirket kodunun elde edilebileceği herhangi bir veri kaynağı sağlamıyorsa, yerleşik [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md) ER işlevini kullanarak `GetCurrentCompany()` formülünü yapılandırın.

> [!NOTE]
> Formüller ER yapılandırmasına özgüdür.

Çalışma zamanında kullanılması gereken e-posta adreslerinin türünü belirtmek için **E-posta gönderilecek adres** iletişim kutusunda **Kime** alanının yanındaki **Düzenle**'yi seçerek **E-posta adresi atayın** açılan iletişim kutusunu açın. Ardından aşağıdaki alanları ayarlayın:

- **Amaç** alanında istediğiniz amaçları seçin. Yalnızca bulunan tarafa ait ilgili kişilerin seçili amaçlarının e-posta adresleri kullanılır.
- Bulunan taraf için yapılandırılan e-posta adresini birincil e-posta adresi olarak kullanmak için **Birincil ilgili kişi** seçeneğini **Evet** olarak ayarlayın.

> [!NOTE]
> **Amaç** alanında amaçlar seçildiyse ve aynı zamanda **Birincil ilgili kişi** seçeneği **Evet** olarak ayarlandıysa, yapılandırılan ölçütlerden en az birini karşılayan her e-posta çalışma zamanında kullanılır.

### <a name="configuration-email"></a>Konfigürasyon e-postası

Kullandığınız yapılandırmanın veri kaynaklarında tek bir e-posta adresi veya noktalı virgüllerle (;) ayrılan birden fazla e-posta adresi döndüren bir düğüm varsa e-posta adresi türü olarak **Yapılandırma e-postası**'nı seçin. Doğru biçimlendirilmiş bir e-posta adresi veya noktalı virgüllerle ayrılan doğru biçimlendirilmiş e-posta adresleri almak için formül tasarımcısında [veri kaynaklarını](general-electronic-reporting.md#FormatComponentOutbound) ve [işlevleri](er-formula-language.md#functions) kullanabilirsiniz. Örneğin, **ISO 20022 Borç Transferi** yapılandırmasını kullanıyorsanız, kapak yazısının gönderilmesi gereken satıcı ilgili kişisi ayrıntılarından alınan satıcı birincil e-posta adresini temsil eden düğüm `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email` düğümüdür.

[![Bir e-posta adresi kaynağını yapılandırma](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Biçim bileşenlerini gruplandırma

Biçim bileşenlerini gruplandırmak için **Elektronik raporlama hedefi** sayfasında **Dosya hedefi** hızlı sekmesinde ızgaradaki bileşenleri seçin ve ardından **Gruplandır**'ı seçin.

**E-posta**, seçili bileşenler için hala kullanılabilir olan önceden yapılandırılmış tek hedeftir. Önceden yapılandırılmış hedefler bileşen grubu için desteklenmediğinden önceden yapılandırılmış başka bir hedef kullanılamaz. Uygun durumlarda, bu değişiklikler size bildirilir.

Daha önce eklediğiniz kayıt, oluşturulan grubun üst bilgisi olarak kabul edilir. Bu üst bilgi kaydında grubun e-posta hedefi ayarları bulunur. Diğer kayıtlar, grubun üst bilgi kaydındaki e-posta hedefi ayarlarını kullanacak olan grup üyeleridir.

Biçim bileşenleri grubunu çözmek için **Dosya hedefi** hızlı sekmesinde gruba ait bir kaydı seçin ve ardından **Grubu Çöz**'ü seçin.

- Bir üst bilgi kaydı seçerseniz grubun tamamı çözülür.
- Bir üye kaydı seçerseniz ve bu kayıt gruptaki son üye kaydıysa grubun tamamı çözülmez.
- Bir gruptaki en son üye kaydı olmayan bir üye kaydını seçerseniz söz konusu kayıt geçerli gruptan dışlanır.

Aşağıdaki çizimde, PDF biçiminde tahsilat mektubunu ve uygun müşteri faturalarını içeren sıkıştırılmış bir giden dosya üretmek üzere yapılandırılmış bir ER biçiminin yapısı gösterilmektedir.

[![Giden belgeler oluşturan bir ER biçiminin yapısı](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

Aşağıdaki çizimde, bu konu başlığında anlatılan şekilde ayrı bileşenleri gruplandırma ve yeni grup için **E-posta** hedefinin etkinleştirilmesi gösterilmektedir. Böylece uygun müşteri faturaları ile birlikte tahsilat mektubunun e-posta ekleri olarak gönderilir.

[![Ayrı bileşenleri gruplandırma ve E-posta hedefini etkinleştirme](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
- [Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)
- [Elektronik raporlamada (ER) formül tasarımcısı](general-electronic-reporting-formula-designer.md)
