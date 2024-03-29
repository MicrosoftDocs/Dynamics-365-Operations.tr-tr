---
title: Sales'teki ilgili kişileri doğrudan Supply Chain Management'taki ilgili kişilerle veya müşterilerle eşitleme
description: Bu makale, Kişiler (Kişiler) ve Kişiler (Müşteriler) varlıklarını Dynamics 365 Sales'dan Dynamics 365 Supply Chain Management'a eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: Henrikan
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 4ddb91c34816791d8eca80e4798eb46c1b496439
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857358"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Sales'teki ilgili kişileri doğrudan Supply Chain Management'taki ilgili kişilerle veya müşterilerle eşitleme

[!include [banner](../includes/banner.md)]



> [!NOTE]
> Aday'dan nakde çözümünü kullanmadan önce [Microsoft Dataverse for Apps için veri tümleştirme](/powerapps/administrator/data-integrator) hakkında bilgi sahibi olmalısınız.

Bu makalede, İlgili Kişi (Kişiler) ve İlgili Kişi (Müşteriler) tablolarını doğrudan Dynamics 365 Sales'den Dynamics 365 Supply Chain Management'a eşitlemekte kullanılan şablonlar ve temel görevler açıklanmaktadır.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Supply Chain Management ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır. Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Supply Chain Management ve Sales arasında veri akışını etkinleştirir. Supply Chain Management ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın. **Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.

Aşağıdaki şablonlar ve temel görevler, İlgili Kişi (Kişiler) tablolarını Sales'dan Supply Chain Management'taki İlgili Kişi (Müşteriler) tablolarına eşitlemekte kullanılır:

- **Veri tümleştirmesindeki şablonların adları:**

    - İlgili kişiler (Sales'ten Supply Chain Management'a) - Doğrudan
    - İlgili kişilerden Müşteriye (Sales'ten Supply Chain Management'a) - Doğrudan

- **Veri tümleştirme projesindeki görevlerin adları**

    - İlgili kişiler
    - ContactToCustomer

Aşağıdaki eşitleme görevi ilgili kişi eşitlemesi gerçekleşemeden önce gereklidir: Hesaplar (Sales'tan Supply Chain Management'a)

## <a name="entity-sets"></a>Varlık kümeleri

| Satışlar    | Supply Chain Management |
|----------|------------------------|
| İlgili kişiler | Dataverse İlgili Kişileri           |
| İlgili kişiler | Müşteriler V2           |

## <a name="entity-flow"></a>Varlık akışı

İlgili Kişiler Sales'ta yönetilir ve Supply Chain Management'a eşitlenir.

Sales'daki bir ilgili kişi, Supply Chain Management'taki bir ilgili kişi veya müşteri olabilir. Sales'deki bir ilgili kişinin Supply Chain Management'a bir ilgili kişi veya müşteri olarak eşitlenip eşitlenmeyeceğini belirlemek için sistem Sales'de ilgili kişinin aşağıdaki özelliklerine bakar:

- **Supply Chain Management içinde bir müşteriye eşitleme:** **Etkin Müşteri** seçeneğinin **Evet** olarak ayarlandığı ilgili kişiler
- **Supply Chain Management'da bir ilgili kişiye eşitleme:** **Etkin Müşteri**'nin **Hayır** olarak ayarlandığı ve **Şirket**'in (Ana Firma/İlgili Kişi) bir hesaba (bir İlgili Kişiye değil) işaret ettiği İlgili Kişiler

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

Yeni bir **Etkin Müşteri** sütunu ilgili kişiye eklendi. Bu sütun satış etkinliğine sahip ilgili kişileri ve satış etkinliğine sahip olmayan ilgili kişileri ayırmak için kullanılır. **Etkin müşteri**, yalnızca ilgili tekliflere, siparişlere veya faturalara sahip ilgili kişiler için **Evet** olarak ayarlanır. Yalnızca bu ilgili kişiler Supply Chain Management'ta müşteriler olarak eşitlenir.

Yeni bir **IsCompanyAnAccount** sütunu ilgili kişiye eklendi. Bu sütun, ilgili kişinin bir **Hesap** türündeki şirkete (ana hesap/ilgili kişi) bağlı olup olmadığını belirtmek için kullanılır. Bu bilgi Supply Chain Management'a ilgili kişiler olarak eşitlenecek ilgili kişileri belirlemek için kullanılır.

**İlgili Kişi Numarası** sütunu, tümleştirme için doğal ve benzersiz anahtarın ilgili kişiye eklendiğinden emin olmak için eklenmiştir. Yeni bir ilgili kişi oluşturulduğunda bir **İlgili Kişi Numarası** değeri otomatik olarak bir numara serisi kullanılarak oluşturulur. Değer **CON**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir. Aşağıda bir örnek verilmiştir: **CON-01000-BVRCPS**

Sales için tümleştirme çözümü uygulandığında, bir yükseltme komut dosyası **İlgili Kişi Numarası** sütununu tüm mevcut ilgili kişiler için daha önce belirtilen numara serisini kullanarak ayarlar. Bir güncelleştirme kodu ayrıca **Etkin Müşteri** sütununu, satış etkinliğine sahip tüm ilgili kişiler için **Evet** olarak ayarlar.

## <a name="in-supply-chain-management"></a>Supply Chain Management'ta

İlgili Kişiler **IsContactPersonExternallyMaintained** özelliğini kullanarak etiketlenir. Bu özellik, belirli bir ilgili kişinin dışarıda tutulduğunu gösterir. Bu durumda, dışarıda tutulan ilgili kişiler, Sales içerisinde tutulur.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

### <a name="contact-to-customer"></a>İlgili kişiden müşteriye

- **CustomerGroup** Supply Chain Management'ta gereklidir. Eşitleme hatalarının önüne geçmek için, eşlemede bir varsayılan değer belirtebilirsiniz. Varsayılan değer daha sonra bu sütun Sales'da boş kalırsa kullanılır.

    Varsayılan şablon değeri **10**'dur.

- Aşağıdaki eşleşmeleri ekleyerek, Supply Chain Management'da gereken el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz. Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.

    - **SiteId** – Bir varsayılan site, Supply Chain Management'taki ürünlerde de tanımlanabilir. Supply Chain Management'ta teklifler ve satış siparişleri oluşturmak için bir site gereklidir.

        **SiteId** için bir şablon değeri tanımlanmamıştır.

    - **WarehouseId** – Bir varsayılan ambar, Supply Chain Management'taki ürünlerde de tanımlanabilir. Supply Chain Management'ta teklifler ve satış siparişleri oluşturmak için bir ambar gereklidir.

        **WarehouseId** için bir şablon değeri tanımlanmamıştır.

    - **LanguageId** - Supply Chain Management'ta teklifler ve satış siparişlerini oluşturmak için bir dil gereklidir.
    
        Varsayılan şablon değeri **tr-tr**'dir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir. 

> [!NOTE]
> Eşleme hangi sütun bilgilerinin Sales'den Supply Chain Management'a eşitleneceğini gösterir.

### <a name="contact-to-contact-example"></a>İlgili kişiden ilgili kişiye örneği

![Veri tümleştirici içerisindeki İlgili kişiden ilgili kişiye şablon eşlemesi.](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer-example"></a>İlgili kişiden müşteriye örneği

![Veri tümleştirici içerisindeki İlgili kişiden müşteriye şablon eşlemesi.](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-articles"></a>İlgili makaleler

[Aday müşteriden nakde](prospect-to-cash.md)

[Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme](accounts-template-mapping-direct.md)

[Supply Chain Management'daki ürünleri doğrudan Sales'deki ürünlerle eşitleme](products-template-mapping-direct.md)

[Sales ve Supply Chain Management arasında satış siparişlerini doğrudan eşitleme](sales-order-template-mapping-direct-two-ways.md)

[Supply Chain Management'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]