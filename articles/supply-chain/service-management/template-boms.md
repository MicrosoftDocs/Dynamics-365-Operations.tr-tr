---
title: Şablon Ürün Reçeteleri
description: Şablon ürün reçetesi (BOM), düzenli olarak servis verilen servis nesnelerinin bileşenlerinin standart bir listesini sağlar.
author: kamaybac
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d34502d74590595f26ba5aae78158ed893a095df
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571319"
---
# <a name="template-boms"></a>Şablon Ürün Reçeteleri

[!include [banner](../includes/banner.md)]

Şablon ürün reçetesi (BOM), düzenli olarak servis verilen servis nesnelerinin bileşenlerinin standart bir listesini sağlar. Şablon ürün reçetesinde listelenen bileşenler servis nesnesinin ayrı ayrı alt bileşenlerini temsil eder. Bir şablon ürün reçetesini bir servis nesnesine uyguladığınızda, servis nesnesinde değiştirilen alt bileşenlerin kaydını tutabilirsiniz.

Şablon ürün reçetesini bir servis anlaşmasına veya servis siparişine uygulamak için onu bir servis nesnesi ilişkisine eklersiniz.

> [!NOTE]
> Her servis nesnesine yalnızca bir şablon ürün reçetesi uygulayabilirsiniz.

## <a name="create-a-template-bom"></a>Şablon ürün reçetesi oluşturma

Aşağıdaki tablo bir şablon ürün reçetesi oluşturmak için kullanabileceğiniz çeşitli yöntemlerle ilgili bilgiler içerir.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Yöntem</p></th>
<th><p>Tanım</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Üretim</p></td>
<td><p>Şablon ürün reçetesi üretim emrini temel alır. Bu seçenek yalnızca bir üretim ortamında iş yapıyorsanız kullanılabilir. Yararı, bir maddeyi oluşturan bileşenlerin güncel ve ayrıntılı bir listesini sağlamasıdır.</p></td>
</tr>
<tr class="even">
<td><p>Madde BOM</p></td>
<td><p>Şablon ürün reçetesi bir madde ürün reçetesini temel alır. Madde ürün reçetesi, üretim ürün reçetesinden farklı olarak bir maddeyi oluşturan bileşenlerin statik listesidir.</p></td>
</tr>
<tr class="odd">
<td><p>Mevcut şablon</p></td>
<td><p>Şablon mevcut bir şablon ürün reçetesini temel alır.</p></td>
</tr>
<tr class="even">
<td><p>El ile</p></td>
<td><p>Bir servis nesnesinde normalde hangi parçaların değiştirildiğini tam olarak biliyorsanız ürün reçetenizi el ile oluşturmayı tercih edebilirsiniz. Bu yöntem, şablona dahil edilen bileşenlerin çalışma alanınızın gerçek gereksinimlerini yansıttığından emin olmanıza yardımcı olur.</p></td>
</tr>
</tbody>
</table>

## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>Şablon ürün reçetesini servis sözleşmesine veya servis siparişine uygulama

Şablon ürün reçetesini servis sözleşmesine, servis siparişine veya her ikisine uygulayabilirsiniz. Servis anlaşması genellikle müşteriyle uzun dönemli bir ilişkiyi kapsar. Servis ürün reçetesine kaydedilen değiştirmelerin geçmişi, servis sözleşmesinde bulunacak kullanışlı verilerdir.

Ayrıca, bir servis nesnesinde gerçekleştirilen bir servisin geçmişini kaydetmek için de bir servis siparişine bir şablon ürün reçetesi uygulayabilirsiniz.

## <a name="copy-the-history-of-a-service-bom"></a>Servis ürün reçetesinin geçmişini kopyalama

Bir servis ürün reçetesi satırının geçmişini bir servis sözleşmesinden diğerine kopyalayabilirsiniz. Servis geçmişini servis sözleşmeleri arasında kopyalayarak bir madde için değiştirme kaydını koruyabilirsiniz.

### <a name="example"></a>Örnek

Bir müşterinin arabası için üç yıllık bir servis anlaşması yaptınız. Bu dönem süresince, müşteri şirketin sunduğu iyi servise alışır. Bu nedenle, sözleşmenin süresi dolduğunda, müşteri yeni bir sözleşme yapmak ister. Artık şirket için daha avantajlı bir anlaşma yapabilirsiniz. Değiştirilen bileşenlerin kaydı gelecekte işinize yarayabileceğinden, servis ürün reçetesinin geçmişini yeni sözleşmeye kopyalarsınız.

## <a name="modify-the-template-bom"></a>Şablon ürün reçetesini değiştirme

Şablon ürün reçetesi bir servis nesnesine eklenmemiş ise, içindeki satırları değiştirebilir veya silebilirsiniz. Şablon ürün reçetesi servis nesnesine eklendikten sonra yalnızca ürün reçetesinin yerel sürümünü değiştirebilirsiniz. Bir şablon ürün reçetesinin yerel sürümünün ayarını çoğaltmak isterseniz, yerel sürümü temel alan yeni bir şablon ürün reçetesi oluşturabilirsiniz. Daha fazla bilgi için bkz. [Servis ürün reçetesini değiştirme](modify-service-bom.md).

Ürün reçetesinde bir maddeyi değiştirirseniz, değiştirme işlemini ürün reçetesi tasarımcısındaki ürün reçetesi satırına kaydedebilirsiniz. İsteğe bağlı olarak, değiştirilen nesne için bir servis siparişi satırı oluşturabilirsiniz. Bir servis siparişi satırı oluşturursanız değiştirilen maddeyi faturalayabilirsiniz. Değiştirme için bir servis siparişi satırı oluşturmazsanız, servis nesnesinin geçmişini izlemek üzere değiştirme kaydı korunur.

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>Ürün reçetesi satırı hakkındaki bilgilerin nasıl görüntüleneceğini değiştirme

Tüm şablon ve servis ürün reçeteleri için ürün reçetesindeki bilgilerin görüntülenme şeklini değiştirebilirsiniz. Değişiklikler tüm şablon ürün reçetelerine ve servis ürün reçetelerine uygulanır. Buna, servis nesnelerine iliştirilenler de dahildir.

## <a name="set-up-number-sequences-for-template-boms"></a>Şablon ürün reçeteleri için numara serileri ayarlama

Şablon ürün reçeteleri kullanmak için iki numara serisi ayarlamanız gerekir. Şablon ürün reçetesi için bir numara serisi ve ürün reçetesi geçmişi satır numarası için bir numara serisi ayarlayın.

> [!NOTE]
> Numara serileri tanımlayıcıları onları gerektiren kayıtlara tahsis etmek için kullanılır. Bir numara serisini bir şablon ürün reçetesi veya ürün reçetesi geçmişi satır numarasına atamak için önce numara serilerinin kodlarını ayarlamanız gerekir.

## <a name="set-up-number-sequences"></a>Numara serileri ayarı

1. **Numara serilerinin** liste sayfasında, şablon ürün reçeteleri ve ürün reçetesi geçmişi satır numarası için numara serileri oluşturun.
1. **Servis yönetimi** \> **Kurulum** \> **Servis yönetimi parametreleri**'ni seçin.
1. **Numara serileri**'ni seçin ve ardından **Numara serileri** formunda oluşturduğunuz numara serisi referansları için bir numara serisi kodu seçin.
1. Değişikliklerinizi kaydetmek için formu kapatın.

> [!NOTE]
> Ürün reçetesi geçmişi satır numarası sistem tarafından ürün reçetesi geçmişi hareketlerini servis sözleşmesi veya servis siparişi ile ilişkilendirmek için kullanılır. Numara kullanıcı arabiriminde görüntülenmez.

## <a name="see-also"></a>Ayrıca bkz.

[Şablon ürün reçetesi oluşturma](create-template-bom.md)

[Nesne ilişkilerinde şablon ürün reçetelerini yönetme](manage-template-boms-on-object-relations.md)

[Servis Ürün Reçetesini Değiştirme](modify-service-bom.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
