---
title: "Sabit kıymet amortisman yöntemleri"
description: "Bu konuda sabit kıymetlerin amortisman yöntemlerine genel bir bakış sunulmuştur."
author: saraschi2
manager: AnnBe
ms.date: 03/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c69fd798c2e978935a63b079fb11c68d8555594c
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="fixed-asset-depreciation-conventions"></a>Sabit kıymet amortisman yöntemleri

[!INCLUDE [banner](../includes/banner.md)]

Amortisman yöntemleri amortismanın, hem sabit kıymetin alındığı hem de sabit kıymetin elden çıkarıldığı yıl için ne zaman ve nasıl hesaplanacağını belirlemek için kullanılır.

Amortisman yöntemleri sabit kıymet grup defteri kurulumuna atanabilir. Bu durumda, atanan amortisman yöntemleri sabit kıymet defterleri oluşturulurken varsayılan değer olarak kullanılır. Amortisman yöntemleri ayrı sabit kıymet defteri üzerinde de ayarlanabilir.


|  Amortisman yöntemi  |                                                                                                                                                                                                                                                                                                                                                                                                     Tanım                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           Hiçbiri            |                                                                                                                                                                                                                                                                                                                                                                     Kıymetlerin amortismanı <strong>Hizmete konma</strong> tarihinde başlar.                                                                                                                                                                                                                                                                                                                                                                      |
|         Yarıyıl         |                                                                                                                                                                                                                                                                                                     Mülke amortisman uyguladığınız ilk ve son sene için yarım senelik amortismanı düşersiniz. Geri kazanma dönemi boyunca diğer her yıl için tam yıllık amortisman düşersiniz.                                                                                                                                                                                                                                                                                                      |
|        Tam ay         |                                                                                                                                                                                                                                                        <strong>Hizmete giriş</strong> tarihi ay içinde herhangi bir zamanda gerçekleşen varlıklar için amortisman ilgili ayın ilk gününden başlar. Ay içinde herhangi bir zamanda geri çekilen varlıklar, amortisman için önceki ayın son gününde geri çekilir.                                                                                                                                                                                                                                                         |
|        Üç aylık dönemin ortası        |                                                                                                           Mülkün hizmete girdiği yıl için amortisman kesintisini hesaplamak üzere, tüm yıla ilişkin amortismanı, aşağıdaki tabloda gösterildiği gibi mülkün hizmete giriş yaptığı çeyreğin yüzdesiyle çarpın.<table><thead><tr><th>Üç aylık dönem</th><th>Yüzde</th></tr></thead><tbody><tr><td>İlk</td><td>87,5</td></tr><tr><td>İkinci</td><td>62,5</td></tr><tr><td>Üçüncü</td><td>37,5</td></tr><tr><td>Dördüncü</td><td>12,5</td></tr></tbody></table>Amortismanın üç aylık döneminin yarısı elden çıkarıldığı çeyreğe alınır (veya tamamen amortisman gerçekleştirilen çeyrek).                                                                                                            |
| Ayın ortası (Ayın 1'i)  | <strong>Hizmete giriş</strong> tarihi ayın ilk yarısında (1 ile 15 arası) olan varlıklar için amortisman <strong>Hizmete giriş</strong> tarihinin gerçekleştiği ayın ilk gününde başlar. <strong>Hizmete giriş</strong> tarihi ayın ikinci yarısında (16 ile ay sonu arası) olan varlıklar için amortisman <strong>Hizmete giriş</strong> tarihinin gerçekleştiği aydan sonraki ayın ilk gününde başlar. Ayın ilk yarısında geri çekilen varlıklar (1. ile 15. gün arasında) önceki ayın son gününde amortisman amacıyla geri çekilmiş olarak kabul edilir. Ayın ikinci yarısında geri çekilen varlıklar (16. gün ile ayın sonu arasında arasında) geri çekildiği ayın son gününde amortisman amacıyla geri çekilmiş olarak kabul edilir. |
| Ayın ortası (Ayın 15'i) |                                                                                                                                                        Mülkü hizmete sunduğunuz yılın amortisman kesintisini hesaplamak için tüm yıl için amortismanı bir kesirle çarpın. Kesirin payı (üstteki sayı) mülkün hizmette olduğu toplam ay sayısı artı 1/2 veya (0,5)'tir. Payda (alttaki sayı ) 12'dir. Mülkü geri kazanma döneminin sonundan önce elden çıkarırsanız, elden çıkardığınız yıl için amortisman kesintisini hesaplamak üzere aynı yöntemi kullanın.                                                                                                                                                        |
| Yarı yıl (yılın başlangıcı) |                                                                                                                                                                                                                                                          <strong>Hizmete giriş</strong> tarihi yılın ilk yarısında olan varlıklar için amortisman yılın (tam yıl) ilk gününde başlar. <strong>Hizmete giriş</strong> tarihi yılın ikinci yarısında olan varlıklar için amortisman yılın ortasında başlar.                                                                                                                                                                                                                                                          |
|   Yarı yıl (sonraki yıl)   |                                                            <strong>Hizmete giriş</strong> tarihi yılın ilk yarısında olan varlıklar için amortisman yılın (tam yıl) ilk gününde başlar. <strong>Hizmete giriş</strong> tarihi yılın ikinci yarısında olan varlıklar için amortisman sonraki yılın ilk gününde başlar. Yılın ilk yarısında geri çekilen varlıklar önceki yılın son gününde amortisman amacıyla geri çekilmiş olarak kabul edilir. Geçerli yıl içinde deftere nakledilen amortismanların tersine çevrilmesi veya ayarlanması gerekir. Yılın ikinci yarısında geri çekilen varlıklar geri çekildikleri yılın son gününde amortisman için geri çekilmiş olarak kabul edilir.                                                            |


