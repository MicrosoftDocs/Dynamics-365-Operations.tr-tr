---
title: E-posta ER hedef türü
description: Bu konu, giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için bir e-posta hedefinin nasıl yapılandırılacağı hakkında bilgi sağlamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72f67ad915ba2acc90ecb52bdb97e42504450a03
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745573"
---
# <a name="email-destination"></a>E-posta hedefi

[!include [banner](../includes/banner.md)]

Giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için bir e-posta hedefi yapılandırabilirsiniz. Hedef ayarına bağlı olarak, oluşturulan bir belge elektronik posta eki olarak teslim edilir.

E-posta ile bir çıkış dosyası göndermek için **Etkin** değerini **Evet** olarak ayarlayın. Bu seçenek etkinleştirildikten sonra e-posta konusunu ve metnini düzenleyebilir ve e-posta alıcılarını belirtebilirsiniz. E-posta metni ve konusu için sabit metinler ayarlayabilir veya ER [formüllerini](er-formula-language.md) kullanarak dinamik e-posta metinleri oluşturabilirsiniz. 

E-posta adreslerini ER içerisinde iki şekilde yapılandırabilirsiniz. Yapılandırma, aynen Yazdırma yönetimi özelliğinin tamamladığı şekilde tamamlanabilir veya bir formülle bir e-posta yapılandırmasına doğrudan başvuru kullanarak bir e-posta adresini çözümleyebilirsiniz.

[![E-posta hedefini etkinleştirme](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>E-posta adresi türleri

**Giden** veya **Bilgi** alanlarında **Düzenle**'yi seçtiğiniz zaman **E-posta at** iletişim kutusu görüntülenir. Daha sonra kullanılacak e-posta adresi türünü seçebilirsiniz. Şu anda **Yapılandırma e-postası** ve **Yazdırma Yönetimi** e-posta türleri destekleniyor.

[![E-posta türü seçme](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Yazdırma yönetimi

**Yazdırma Yönetimi** e-posta türünü seçerseniz, **Giden** alanına sabit bir e-posta adresi girebilirsiniz. 

[![Sabit e-posta adreslerini yapılandırma](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Sabit olmayan e-posta adreslerini kullanmak amacıyla bir dosya hedefi için e-posta kaynak türünü seçmelisiniz. Aşağıdaki değerler desteklenir: **Müşteri**, **Satıcı**, **Müşteri Adayı**, **İlgili kişi**, **Rakip**, **Çalışan**, **Başvuran**, **Satıcı adayı** ve **Onaylanmamış satıcı**. Bir e-posta kaynak türü seçtikten sonra **Formül tasarımcısı** formunu açmak için **E-posta kaynak hesabı** alanının yanındaki düğmeyi kullanın. Bu formu çalışma zamanında dönen bir formülü, seçilen kaynak türünün **taraf hesabını** işlenmiş belgeden e-posta hedefine iliştirmek için kullanabilirsiniz.

[![E-posta kaynağı hesabını yapılandırma](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Formüller ER yapılandırmasına özgüdür. **Formül** alanında bir müşteri veya satıcı tarafı türü için belgeye özgü bir referans girin. Yazmak yerine, müşteri veya satıcı hesabını temsil eden bir veri kaynağı düğümünü bulabilir ve sonra formülü güncelleştirmek için **Veri kaynağı ekle**'yi seçebilirsiniz. Örneğin, **ISO 20022 Borç Transferi** yapılandırmasını kullanıyorsanız bir satıcı hesabını temsil eden düğüm `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID` olur.

`"DE-001"` gibi bir dize değeri girer ve bir formül kaydederseniz, satıcının ilgili kişisine ( **DE-001**) bir e-posta gönderilir.


[![ER formül tasarımcısı sayfası](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![E-posta kaynağı öznitelik hesabını yapılandırma](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>Konfigürasyon e-postası

Kullandığınız yapılandırma, veri kaynaklarında bir **e-posta adresini** döndüren bir düğüme sahipse bu e-posta türünü kullanın. Formül tasarımcısında veri kaynaklarını ve fonksiyonları, doğru şekilde biçimlendirilmiş bir e-posta adresi elde etmek için kullanabilirsiniz. Örneğin, **ISO 20022 Borç Transferi** yapılandırmasını kullanıyorsanız bir satıcının ilgili kişi e-posta adresini temsil eden düğüm `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email` olur.

[![E-posta adresi kaynağını yapılandırma](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
- [Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)
- [Elektronik raporlamada (ER) formül tasarımcısı](general-electronic-reporting-formula-designer.md)
