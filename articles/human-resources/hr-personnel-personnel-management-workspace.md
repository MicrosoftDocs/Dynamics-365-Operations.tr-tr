---
title: Personel yönetimi çalışma alanı
description: Bu makalede, Personel yönetimi çalışma alanının kavramsal öğeleri açıklanmaktadır.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fc424905bc9311662859b900636a68de2f7ee3cb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888773"
---
# <a name="personnel-management-workspace"></a>Personel yönetimi çalışma alanı


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Personel yönetimi** çalışma alanı çok büyük miktarda içerik içerir. Personel hareketlerini içerir, personel değişikliklerini, açık pozisyonları, adres değişikliklerini, tarihi sona eren kayıtları ve analizi izler ve belirli bilgilere bağlantılar sağlar. Bu makalede çalışma alanının her bölümü hakkında ayrıntılı bilgiler sağlanmaktadır.

## <a name="activity-tab"></a>Faaliyet sekmesi

**Faaliyet** sekmesi, çalışanları çalışma sürecindeki aşamalarına göre gruplayan bölümler içerir:

- **İşe alınacak adaylar**
- **Yakında başlıyor**
- **En son işe almalar**
- **Çıkış**
- **Çıktı**

Bir çalışan bu aşamaların birinde olduğunda belirli eylemler karttaki bir düğme olarak veya sağ üst köşedeki üç noktayı (**...**) seçtiğinizde görüntülenen menüde kullanılabilir olur. Aşağıdaki alt bölümler **Faaliyet** sekmesinin bölümlerini açıklar ve kullanılabilir eylemleri listeler.

### <a name="candidates-to-hire"></a>İşe alınacak adaylar

Çalışma alanının **İşe alınacak adaylar** bölümü, birden çok kaynaktan doldurulur:

- Açık Veri Protokolü (OData) varlığı
- LinkedIn tümleştirmesi
- Ürüne el ile girilen veriler

Aday **İşe alınacak adaylar** bölümünde göründüğünde, aday kartındaki üç noktayı seçerek aşağıdaki eylemleri gerçekleştirebilirsiniz:

- **Adayı bırakın.**
- **İşe alma**
- **İşe Al**

> [!NOTE]
> Aday listesi Microsoft Dataverse'den dolduruluyorsa, aday ile bir tüzel kişilik ilişkilendirilmediğinden, aynı adaylar tüm tüzel kişiliklerde görüntülenecektir.

### <a name="starting-soon"></a>Yakında başlıyor

**Yakında başlayacak** bölümünde gelecekte bir başlangıç tarihi olan çalışanlar listelenir. Liste başlama tarihine göre sıralanır. Bugünün verilerine en yakın olan başlangıç tarihi ilk olarak listelenir.

Yönetici kart üzerinde görünmüyorsa, çalışan için bir pozisyon atanmamıştır.

> [!NOTE] 
> Denetim listesini uygulamadan önce bir çalışana pozisyon atamanızı öneririz. Bazı durumlarda, ekleme görevleri, yeni işe alınan bir çalışanın yöneticisine atanır. Ancak, hiçbir pozisyon atanmadığı takdirde, yeni çalışanın yöneticisi saptanamaz. Bu durumda, yöneticiye yönelik ekleme görevleri, bunun yerine onay listesi sahibine atanacaktır.

Çalışanlar **Yakında başlayacak** bölümünde göründüğünde, bunlar için aşağıdaki eylemler kullanılabilir:

- Pozisyon ata
- İstihdamı doğrula
- Sabit ücret ata
- Değişken ücret ata
- Hiyerarşide görüntüleme
- Yapılacaklar listesini uygula\*\*

\*\* Bu eylem, varsayılan eylemdir. Kart üzerinde bir düğme olarak görünür.

### <a name="recent-hires"></a>En son işe almalar

**En son işe alımlar** bölümü, en yakın geçmişte başlangıç tarihi olan çalışanları listeler. Liste başlama tarihine göre sıralanır. Bugünün tarihine en yakın olan başlangıç tarihi ilk olarak listelenir.

Varsayılan olarak, liste son yedi gün içinde işe alınan çalışanları gösterir. Bu ayarı değiştirmek için, **İnsan Kaynakları parametreleri** sayfasında, **Genel** sekmesinde **En son işe alımlar** için bir zaman dilimi belirleyin. **En son işe alımlar** bölümündeki veriler belirli sayıda gün, ay veya yıl için gösterilebilir. Örneğin, son 14 günde işe alınan çalışanların listesini görüntülemek için, **Dönem** alanını **14** olarak ve **Birim** alanını **Gün** olarak ayarlayın.

> [!NOTE]
> **İnsan Kaynakları parametreleri** sayfasındaki ayarlar şirkete özeldir. Bu nedenle, en son işe alımlar için görüntülediğiniz zaman dilimi şirkete göre farklılık gösterebilir. Örneğin, USMF şirketinde, son yedi gündeki tüm yeni işe alımları görmek isteyebilirsiniz. Ancak, USSI şirketinde, son 14 gündeki tüm yeni işe alımları görmek isteyebilirsiniz. Bu durumda, her şirkette **İnsan Kaynakları parametreleri** sayfasını açın ve parametreleri gerektiği gibi ayarlayın.

Yönetici kart üzerinde görünmüyorsa, çalışan için bir pozisyon atanmamıştır.

Çalışanlar **En son işe alımlar** bölümünde göründüğünde, bunlar için aşağıdaki eylemler kullanılabilir:

- Pozisyon ata
- İstihdamı doğrula
- Sabit ücret
- Değişken ücret ata
- Hiyerarşide görüntüle
- Yapılacaklar listesini uygula\*\*

\*\* Bu eylem, varsayılan eylemdir. Kart üzerinde bir düğme olarak görünür.

### <a name="exiting"></a>Çıkış

**Çıkış yapan** bölümünde gelecekte bir iş sonlandırma tarihi olan çalışanlar listelenir. Liste işin sonlandırılma tarihine göre sıralanır. Bugünün tarihine en yakın olan sonlandırma tarihi ilk olarak listelenir. 

Varsayılan olarak, liste sonlandırma tarihi gelecek yedi gün içinde olan çalışanları gösterir. Bu ayarı değiştirmek için, **İnsan Kaynakları parametreleri** sayfasında, **Genel** sekmesinde **Çıkış yapan çalışanları görüntüle** için bir zaman dilimi belirleyin. **Çıkış yapan** bölümündeki veriler belirli sayıda gün, ay veya yıl için gösterilebilir. Örneğin, gelecek 14 günde işten çıkarılacak çalışanların listesini görüntülemek için, **Dönem** alanını **14** olarak ve **Birim** alanını **Gün** olarak ayarlayın.

Çalışanlar **Çıkış yapan** bölümünde göründüğünde, bunlar için aşağıdaki eylemler kullanılabilir:

- Yapılacaklar listesini uygula\*\*
- İstihdamı doğrula
- Hiyerarşide görüntüleme

\*\* Bu eylem, varsayılan eylemdir. Kart üzerinde bir düğme olarak görünür.

### <a name="exited"></a>Çıktı

**Çıktı** bölümü, en yakın geçmişteki sonlanma tarihine sahip çalışanları listeler. Liste işin sonlandırılma tarihine göre sıralanır. Bugünün tarihine en yakın olan sonlandırma tarihi ilk olarak listelenir.

Varsayılan olarak, liste sonlandırma tarihi geçmiş yedi gün içinde olan çalışanları gösterir. Bu ayarı değiştirmek için, **İnsan Kaynakları parametreleri** sayfasında, **Genel** sekmesinde **Çıkan çalışanları görüntüle** için bir zaman dilimi belirleyin. **Çıktı** bölümündeki veriler belirli sayıda gün, ay veya yıl için gösterilebilir. Örneğin, son 14 günde işine son verilen çalışanların listesini görüntülemek için, **Dönem** alanını **14** olarak ve **Birim** alanını **Gün** olarak ayarlayın.

Çalışan **Çıktı** bölümünde göründüğünde, bunlar için aşağıdaki eylemler kullanılabilir:

- Yapılacaklar listesini uygula\*\*
- İstihdamı doğrula
- Hiyerarşide görüntüle

\*\* Bu eylem, varsayılan eylemdir. Kart üzerinde bir düğme olarak görünür.

## <a name="employee-changes-tab"></a>Personel değişiklikleri sekmesi

**Personel değişiklikleri** sekmesi tüm çalışan personel eylemlerinin listesini sağlar. Bu liste varsayılan olarak kullanılamaz. İşlevi etkinleştirmek için **İnsan Kaynakları paylaşılan parametreleri** sayfasında, **Personel eylemleri** sekmesinde, **Çalışan eylemlerini etkinleştir** seçeneğini **Evet** olarak ayarlayın.

## <a name="position-changes-tab"></a>Pozisyon değişiklikleri sekmesi

**Pozisyon değişiklikleri** sekmesi tüm pozisyon personel eylemlerinin listesini sağlar. Bu liste varsayılan olarak kullanılamaz. İşlevi etkinleştirmek için **İnsan Kaynakları paylaşılan parametreleri** sayfasında, **Personel eylemleri** sekmesinde, **Pozisyon eylemlerini etkinleştir** seçeneğini **Evet** olarak ayarlayın.

## <a name="open-positions-tab"></a>Açık pozisyonlar sekmesi

**Açık pozisyonlar** sekmesi tüm açık pozisyonları listeler. Listede gözükmeleri için, pozisyonların bugün veya öncesindeki bir etkinleştirme tarihine sahip olmaları ve geçerli bir çalışan ataması içermeleri gerekir.

> [!NOTE]
> Liste, çalışan atamasını bugün itibarıyla dikkate alır. Gelecek tarihli bir çalışan atamasına sahip herhangi bir pozisyon listede görüntülenmeye devam eder. Ancak, çalışan atamasının geçerlilik tarihine ulaşıldığında, pozisyon listeden kaldırılır.

## <a name="expiring-records-tab"></a>Süresi dolan kayıtlar sekmesi

**Süresi dolan kayıtlar** sekmesinde, kullanıcının oturum açtığı şirketteki çalışanlar için süresi dolmuş veya süresi dolacak olan tüm maddeler listelenir. Listede aşağıdaki öğeler görünür:

- **Sertifikalar**
- **Kimlik**
- **Denemeler**
- **Filtrelemeler**
- **Sınamalar**

Listenin süresi dolan kayıtları mı yoksa süresi dolmak üzere olan kayıtları mı göstereceğini belirtmek için **İnsan Kaynakları parametreleri** sayfasında, **Genel** sekmesinde **Süresi dolmak üzere olan kayıtlar** veya **Süresi dolan kayıtlar** için bir zaman dilimi tanımlayın. **Süresi dolmak üzere olan kayıtlar** sekmesindeki veriler belirli bir gün sayısı için görüntülenebilir. Örneğin, sonraki 14 günde süresi dolacak kayıtların listesini görmek için **Gün sayısı** alanını **14** olarak ayarlayın.

> [!NOTE] 
> **Süresi dolan kayıtlar** veya **Süresi dolmak üzere olan kayıtlar** için zaman dilimini **İnsan kaynakları parametreleri** sayfasında **0** olarak ayarlarsanız liste bu kayıtlardan hiçbirini göstermez.

## <a name="employees-tile"></a>Personel kutucuğu

**Personel** kutucuğu kullanıcının o anda oturum açtığı şirkette istihdam edilen tüm çalışanların sayısını sağlar. **Personel** kutucuğunu seçtiğinizde, yeni bir sayfada personel ayrıntıları gösterilir.

## <a name="contractors-tile"></a>Yükleniciler kutucuğu

**Yükleniciler** kutucuğu kullanıcının o anda oturum açtığı şirkette istihdam edilen tüm yüklenicilerin sayısını sağlar. **Yükleniciler** kutucuğunu seçtiğinizde, yeni bir sayfada yüklenici ayrıntıları gösterilir.

## <a name="open-positions-tile"></a>Açık pozisyonlar kutucuğu

**Açık pozisyonlar** kutucuğu tüm açık pozisyonların sayısını sağlar. **Açık pozisyonlar** kutucuğunu seçtiğinizde, yeni bir sayfada açık pozisyonların ayrıntıları gösterilir. Sayıya eklenmeleri için, pozisyonların bugün veya öncesindeki bir etkinleştirme tarihine sahip olmaları ve geçerli bir çalışan ataması içermeleri gerekir.

> [!NOTE]
> Kutucuk, çalışan atamasını bugün itibarıyla dikkate alır. Gelecek tarihli bir çalışan atamasına sahip herhangi bir sayıya dahil edilmeye devam eder. Ancak, çalışan atamasının geçerlilik tarihine ulaşıldığında, pozisyon sayının dışında bırakılır.

## <a name="approvals-tile"></a>Onaylar kutucuğu

**Onaylar** kutucuğu, geçerli kullanıcının onayını bekleyen tüm iş akışı öğelerinin sayısını sağlar. **Onaylar** kutucuğunu seçtiğinizde, yeni bir sayfa onayınızı gerektiren iş akışı öğelerinin ayrıntılarını gösterir.

## <a name="address-changes-tile"></a>Adres değişiklikleri kutucuğu

**Adres değişiklikleri** kutucuğu, **İnsan Kaynakları parametreleri** sayfasında belirtilen gün sayısı boyunca gerçekleşen tüm adres değişikliklerinin sayısını sağlar. **Adres değişiklikleri** kutucuğunu seçtiğinizde, yeni bir sayfa, tüm adres değişikliklerinin ayrıntılarını görüntüler. Sayfanın sağ üst köşesinde, gelecek tarihteki adres değişikliklerini görüntülemek için **Gelecek adres değişikliklerini dahil et**'i seçebilirsiniz.

Adres değişikliklerinin nasıl görüntüleneceği ve yönetileceği hakkında daha fazla bilgi için bkz. [Adres değişikliklerini görüntüleme ve yönetme](hr-personnel-view-address-changes.md).
