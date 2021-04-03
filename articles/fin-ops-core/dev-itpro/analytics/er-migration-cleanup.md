---
title: ER geçiş temizleme
description: Bu konu, ER şablonları ile ilgili sorunları gidermek için ER geçiş temizleme işlevini nasıl kullanabileceğinizi açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: b09afc30c401e2dccfc4114261dc5e713c8c470c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565527"
---
# <a name="er-migration-cleanup"></a>ER geçişi temizleme 

[!include[banner](../includes/banner.md)]

Finance kurulumlarınızı yönetirken, geçerli kurulumu başka bir konuma geçirmeye karar verebilirsiniz. Örneğin, üretim örneğinizi yeni bir korumalı alan ortamına geçirebilirsiniz. Elektronik Raporlama (ER) çerçevesini Microsoft Azure Blob depolamada şablon depolamak üzere yapılandırırsanız, yeni korumalı alan ortamındaki **DocuValue** tablosu, üretim ortamındaki Blob depolama örneğine başvurur. Ancak, geçiş işlemi Blob depolamadaki yapıların geçirilmesini desteklemediğinden, bu örneğe korumalı alan ortamından erişilemez. Bunun yerine, yeni korumalı alan ortamında, henüz ER şablonlarını elde etmemiş olan korumalı alan ortamındaki BLOB depolaması örneğine başvurursunuz.

İiş belgeleri oluşturmak için şablon kullanan bir ER biçimini çalıştırmaya çalışırsanız bir özel durum oluşur ve eksik şablon hakkında bilgilendirilirsiniz. Ayrıca, şablonu içeren ER biçimi yapılandırmasını silmek ve yeniden içe aktarmak için ER geçiş temizleme seçeneğini de kullanabilirsiniz.

[![ER biçimi çalıştırma](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

**Yapılandırmalar** sayfasına giderseniz (**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**) ve yapılandırmalar ağacında, şablon kullanan bir ER biçimi yapılandırmasını silmeye çalışırsanız benzer bir hata alırsınız.

[![ER biçimi silme](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

Erişemediğiniz ER şablonlarınız ile ilgili sorunları gidermek için aşağıdaki adımları tamamlayın.

1.  **Kuruluş Yönetimi** \> **Periyodik** \> **Geçiş temizleme** sayfasına gidin.
2.  Yürütülemeyen veya silinemeyen bir ER biçimi yapılandırması seçin.
3.  **Sil**'i seçin.
4.  Seçili ER biçimi yapılandırmasını silme işlemini onaylayın.
5.  Silinen ER biçimi yapılandırmasını geçerli Finance kurulumuna [aktarın](download-electronic-reporting-configuration-lcs.md).

## <a name="applicability"></a>Uygulanabilirlik

> [Önemli] **Geçiş temizleme** seçeneği yalnızca erişilemeyen ER şablonları içeren ER biçim yapılandırmalarına yöneliktir. **Geçiş temizleme** seçeneğini kullanarak bir ER biçimi yapılandırmasını sildiğinizde , ER yalnızca uygulama veritabanındaki yapılandırma yapılarına ilişkin şablonları siler. Blob depolama alanında uygun fiziksel dosyaların varlığı doğrulanmaz. Bunun yerine, bunların yok olduğu varsayılır. Bu nedenle, **Yapılandırmalar** sayfasındaki ER yapılandırma silme seçeneğine alternatif olarak **Geçiş temizleme** seçeneğini kullanmayın. **Geçiş temizleme** seçeneğini yalnızca **Yapılandırmalar** sayfasındaki ER yapılandırması silme seçeneği başarısız olduğunda kullanın.
>
> Başvurulan şablon Blob depolamada kullanılabilir durumdayken bir ER biçimi yapılandırmasını silmek için **Geçiş temizleme** seçeneğini kullanırsanız, yalnozca uygulama veritabanındaki ilgili yapılandırma yapılarını silersiniz. Blob depolama alanındaki şablonun fiziksel dosyası kalır. Blob depolama alanında dosya üzerine yazmaya artık izin verilmez. Daha fazla bilgi için bkz. [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217). Ek olarak, bu ortamdaki Geçiş temizleme özelliği kullanılarak silinen yapılandırmaların artık yeniden içe aktarılması mümkün olmayacaktır. Bu sorunu gidermek için, karşılık gelen dosyayı Blob depolama alanında bulmanız ve el ile silmeniz gerekir.

[![ER biçimini içe aktarma](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

Uygulama örneğinizi bir kereden fazla geçiş hedefi olarak kullanılan ve Blob depolamanın zaten ER şablon dosyalarını içerdiği başka bir konuma geçirdiğinizde benzer bir sorun oluşabilir.

Birden fazla ER biçimi yapılandırmanız olabileceğinden bu işlem uzun sürebilir. Bu nedenle, bozuk başvuruları olan şablonları otomatik olarak kurtarmak için [ER şablonları için yedek depolama](er-backup-storage-templates.md) özelliğinin kullanılması tercih edilir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]