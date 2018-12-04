--- 
title: "ER Hedefleri yapılandırma"
description: "Bu yordamda bir klasör veya bir dosya gibi Elektronik raporlama (ER) çıkış bileşenleri için farklı hedeflerin nasıl ayarlanacağı ve kullanılacağı gösterilmiştir."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 83c6b8db609b83f94b51800616976eb9ce08d79b
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="er-configure-destinations"></a>ER Hedefleri yapılandırma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordamda bir klasör veya bir dosya gibi Elektronik raporlama (ER) çıkış bileşenleri için farklı hedeflerin nasıl ayarlanacağı ve kullanılacağı gösterilmiştir. Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir. Almanya, tüzel kişiliğin ana adresinin bulunduğu ülke\bölgedir, ancak bu yordam için herhangi bir tüzel kişilik kullanabilirsiniz. 

Bu örnekte kullanılan biçim, ISO20022 Borç transferidir ancak daha önce içe aktardığınız herhangi bir formatı kullanabilirsiniz. Bu yordamın bir tekli dosya ve tek bir hedef kurulumuna örnek olduğuna dikkat edin. Elektronik raporlama hedef yönetimi hakkında daha fazla bilgiyi Dynamics 365 for Finance and Operations Help Wiki altında bulabilirsiniz.

1. Sırasıyla Organizasyon yönetimi > Elektronik raporlama > Elektronik raporlama hedefi seçimlerini yapın.
2. Bir format için yeni bir hedef kümesi oluşturmak için Yeni düğmesini tıklayın.
3. Başvuru alanında hedefleri yapılandırmak istediğiniz bir format seçin.
    * Seçilebilecek bir değer bulunmuyorsa, herhangi bir Elektronik raporlama formatı yapılandırmasını içeri aktarmamışsınızdır. Hedefleri ayarlamadan önce bir format yapılandırmasını içe aktarmanız gerekir.  
4. Yeni bir dosya hedefi oluşturmak için Yeni düğmesine tıklayın.
    * Klasör veya dosya gibi aynı formattaki her bir çıkış bileşeni için bir dosya hedefi oluşturabileceğinizi dikkate alın. Hedefleri ayarlardan ayrı olarak etkinleştirebilir ve devre dışı bırakılabilirsiniz.  
5. Ad alanında, çıkış bileşeni için anlaşılması kolay bir ad girin.
    * "Ödeme dosyası" veya "Denetim raporu" gibi anlamlı adlar kullanmanızı öneririz. Bu adlar, hedef ayarlarının yanı sıra yapılandırma çalışma süresince kullanıcılara gösterilecektir.  
6. Dosya adında, formata özel bir dosya veya klasör seçin.
7. Ayarlar öğesini tıklayın.
8. Etkinleştirilen alanından 'Evet'i seçin.
    * Her bir sekmedeki Etkin onay kutusu, her bir hedefi ayrı olarak etkinleştirir ve devre dışı bırakır. Bu örnekte, dosya oluşturulduğunda bir posta alıcısına bir çıkış dosyası gönderilmesini etkinleştireceksiniz.  
9. E-posta alıcılarını ayarlamak için Düzenle'ye tıklayın.
10. Ekle öğesini tıklatın.
11. Yazdırma Yönetimi e-postası'na tıklayın.
12. E-posta kaynağı alanından bir seçeneği belirleyin.
    * Müşteri veya satıcı türü gibi farklı e-posta kaynağı türleri seçebilirsiniz. Bu da E-posta kaynak hesap formülü tarafından oluşturulan bağımsız değişken türünü tanımlar. Aşağıdaki adımda açıklanan E-posta kaynak hesabı formülü, bir e-posta kaynağını bağlayacağınız yerdir. Formül bir satıcı hesabı üretiyorsa Satıcıyı seçin. ISO 20022 Borç Transferi yapılandırma örneği kullanıyorsanız Satıcıyı kullanın.  
13. E-posta kaynağını bağla düğmesine tıklayın.
14. Formülde, daha önce seçtiğiniz taraf türü için belgeye özel bir referans girin.
    * Yazmak yerine, taraf hesabını temsil eden bir veri kaynağı düğümünü bulabilir ve formülü güncelleştirmek için Veri kaynağı ekle düğmesini tıklayabilirsiniz. Örneğin; ISO 20022 Borç Transferi yapılandırmasını kullanıyorsanız bir satıcı hesabını temsil eden düğüm '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID olacaktır. Aksi takdirde, bir formül kaydetmek için "DE-001" gibi, herhangi bir dize değeri girin.  
15. Kaydet'e tıklayın.
16. Sayfayı kapatın.
17. Tarafın ilgili kişi ayrıntılarını yapılandırmak için Düzenle'ye tıklayın.
18. Birincil kişi alanında 'Evet'i seçin.
    * Bu hedef için e-posta adresi olarak kullanılması gereken taraf ilgili kişisi türünü göstermek için farklı seçenekleri kullanabilirsiniz. Bu örnekte birincil ilgili kişiyi kullanıyoruz.  
19. Tamam'a tıklayın.
20. Tamam'a tıklayın.
21. Konu alanına bir değer yazın.
22. Tamam'a tıklayın.


