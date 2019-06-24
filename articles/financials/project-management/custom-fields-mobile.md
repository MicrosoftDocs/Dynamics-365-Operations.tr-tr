---
title: iOS ve Android üzerinde Microsoft Dynamics 365 Project Timesheet mobil uygulaması için özel alanlar uygulamak
description: Bu konu, özel alanları uygulamak için uzantıların kullanımıyla ilgili yaygın desenler sağlar.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 19859d8566a8c7840066b2c10c6b08b67f1b83f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2019
ms.locfileid: "1618008"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>iOS ve Android üzerinde Microsoft Dynamics 365 Project Timesheet mobil uygulaması için özel alanlar uygulamak

[!include [banner](../includes/banner.md)]

Bu konu, özel alanları uygulamak için uzantıların kullanımıyla ilgili yaygın desenler sağlar. Aşağıdaki konular el alınmaktadır:

- Özel alan çerçevesinin desteklediği çeşitli veri türleri
- Zaman çizelgesi girişlerinde salt okunur veya düzenlenebilir alanları gösterme ve kullanıcı tarafından sağlanan değerleri veritabanına geri kaydetme
- Zaman çizelgesi üstbilgisinde salt okunur alanlar nasıl gösterilir
- Diğer özel iş mantığı, alanlardaki varsayılan değerleri girmek ve ek doğrulama yapmak için nasıl tümleştirilir

## <a name="audience"></a>Hedef Kitle

Bu konu, kendi özel alanlarını Apple iOS ve Google Android için mevcut Microsoft Dynamics 365 Project Timesheet mobil uygulamasına tümleştirmek isteyen geliştiriciler içindir. Varsayım, okuyucuların X++ geliştirme ve proje zaman çizelgesi işlevleri hakkında bilgi sahibi olduğunu varsayar.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Veri sözleşmesi – TSTimesheetCustomField X++ sınıfı

**TSTimesheetCustomField** sınıfı, zaman çizelgesi işlevselliği için özel bir alanla ilgili bilgileri temsil eden X++ veri sözleşmesi sınıfıdır. Özel alan nesnelerinin listeleri, hem TSTimesheetDetails veri sözleşmesine hem de bir mobil uygulamadaki özel alanları göstermek için TSTimesheetEntry veri sözleşmesine geçirilir.

- **TSTimesheetDetails** - Zaman çizelgesi başlık sözleşmesi.
- **TSTimesheetEntry** - Zaman çizelgesi hareket sözleşmesi. Bu nesnelerin aynı proje bilgilerine ve **timesheetLineRecId** değerine sahip grupları bir satır oluşturur.

### <a name="fieldbasetype-types"></a>fieldBaseType (Türler)

**TsTimesheetCustom** nesnesindeki **FieldBaseType** özelliği, uygulamada görünen alanın türünü belirler. Desteklenen **Türler** değerleri aşağıdaki gibidir.

| Türler değeri | Türü              | Notlar |
|-------------|-------------------|-------|
| 0           | Dize (ve Enum) | Alan bir metin alanı olarak görünür. |
| 1           | Tamsayı           | Değer, ondalık basamak içermeyen bir sayı olarak gösterilir. |
| 2           | Gerçek              | Değer, ondalık basamak içeren bir sayı olarak gösterilir.<p>Gerçek değeri uygulamadaki bir para birimi olarak göstermek için **fieldExtenededType** özelliğini kullanın. Gösterilen ondalık basamak sayısını ayarlamak için **numberOfDecimals** özelliğini kullanabilirsiniz.</p> |
| 3           | Tarih              | Tarih biçimleri **Kullanıcı seçeneklerinde**, **Dil ve ülke/bölge tercihlerinde** altında belirtilen **Tarih, saat ve sayı biçimi** ayarıyla belirlenir. |
| 4           | Boole           | |
| 15          | GUID              | |
| 16          | Int64             | |

- **TSTimesheetCustomField** nesnesinde **stringOptions** özelliği sağlanmadıysa, kullanıcıya bir serbest metin alanı sağlanır.

    **stringLength**özelliği, kullanıcıların girebileceği maksimum dize uzunluğunu ayarlamak için kullanılabilir.

- **TSTimesheetCustomField** nesnesinde **stringOptions**özelliği sağlanmışsa, kullanıcıların seçenek düğmelerini (radyo düğmeleri) kullanarak seçim yapabilen tek değerleri bu liste öğeleridir.

    Bu durumda, dize alanı kullanıcı girişi amacıyla bir enum değeri olarak davranabilir. Değeri veritabanına bir enum olarak kaydetmek için, komut zinciri kullanarak veritabanına kaydetmeden önce dize değerini el ile numaralama değerine geri eşleyin (bir zaman çizelgesi girdisini uygulamadan önce, bir Timesheet girişini kullanarak yeniden görüntülemek için "Veritabanına uygulamadan geri TSTimesheetEntryService sınıfı üzerinde bir komut zinciri kullanın" bölümünde bir örnek olarak da yer almaktadır).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Gerçek değerleri para birimi olarak biçimlendirmek için bu özelliği kullanabilirsiniz. Bu yaklaşım yalnızca **fieldBaseType** değeri **Gerçek** ise uygulanabilir.

- **TSCustomFieldExtendedType:None** – Biçimlendirme uygulanmaz.
- **TSCustomFieldExtendedType::Currency** – Değeri para birimi olarak biçimlendir.

    Para birimi biçimlendirmesi etkin olduğunda, **stringValue** alanı, uygulamada gösterilmesi gereken para birimi kodunu geçirebilir. Bu değer salt okunur bir değerdir.

    **realValue** alanı, veritabanına kaydedilmesi gereken para tutarını içerir.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Özel alanın uygulamada nerede görüneceğini belirtmek için bu özelliği kullanabilirsiniz.

- **TSCustomFieldSection::Header** – Alan, uygulamanın **Daha fazla ayrıntı görüntüle** bölümünde görüntülenir. Bu alanlar her zaman salt okunurdur.
- **TSCustomFieldSection::Line** – Alan, zaman çizelgesi girişlerinde diğer tüm kullanıma hazır satır alanlarından sonra görünür. Bu alanlar düzenlenebilir ya da salt okunur olabilir.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Bu özellik, uygulamanın sağladığı değerler veritabanına geri kaydedildiğinde alanı tanımlar.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Bu özellik, uygulamanın sağladığı değerler veritabanına geri kaydedildiğinde alanı tanımlar.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Bu özelliği, alanın zaman çizelgesi girişi bölümünde kullanıcılar tarafından düzenlenebilir olduğunu belirtmek için **Evet** olarak ayarlayın. Özelliği **Hayır** olarak ayarlayarak alanı salt okunur yapın.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Bu özelliği, alanın zaman çizelgesi girişi bölümünde zorunlu olduğunu belirtmek için **Evet** olarak ayarlayın.

### <a name="label-str"></a>etiket (str)

Bu özellik, uygulama içinde alanın yanında gösterilen etiketi belirtir.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Dizeler listesi)

Bu özellik, yalnızca **fieldBaseType**, **Dize** olarak ayarlandıysa uygulanabilir. **stringOptions** ayarlanmışsa, seçenek düğmeleri (radyo düğmeleri) aracılığıyla seçim için kullanılabilen dize değerleri listedeki dizelerle belirtilir. Hiçbir dize sağlanmazsa, dize alanındaki serbest metin girişine izin verilir (Bu konunun ilerleyen kısımlarında yer alan "Uygulamadan bir zaman çizelgesi girdisini veritabanına geri kaydetmek için TSTimesheetEntryService sınıfı üzerinde komut zinciri kullan" bölümüne bakın).

### <a name="stringlength-int"></a>stringLength (int)

Bu özellik bir dize alanı için maksimum uzunluğu belirtir. Yalnızca **fieldBaseType**, **Dize** olarak ayarlandıysa uygulanabilir.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Bu özellik, gerçek bir alan için gösterilen ondalık basamak sayısını belirtir. Yalnızca **fieldBaseType**, **Gerçek** olarak ayarlandıysa uygulanabilir.

### <a name="ordersequence-int"></a>orderSequence (int)

Bu özellik, birden çok özel alan belirtildiğinde, özel alanların uygulamada gösterilme sırasını denetler. Daha düşük sayıya sahip alanlar önce gösterilir.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

**Boole** türü alanlar için bu özellik alanın Boole değerini sunucu ve uygulama arasında iletir.

### <a name="guidvalue-guid"></a>guidValue (guid)

**GUID** türü alanlar için bu özellik alanın genel benzersiz kimlik tanımlayıcı (GUID) değerini sunucu ve uygulama arasında iletir.

### <a name="int64value-int64"></a>int64Value (int64)

**Int64** türü alanlar için bu özellik alanın int64 değerini sunucu ve uygulama arasında iletir.

### <a name="intvalue-int"></a>intValue (int)

**Int** türü alanlar için bu özellik alanın int değerini sunucu ve uygulama arasında iletir.

### <a name="realvalue-real"></a>realValue (gerçek)

**Gerçek** türü alanlar için bu özellik alanın gerçek değerini sunucu ve uygulama arasında iletir.

### <a name="stringvalue-str"></a>stringValue (str)

**Dize** türü alanlar için bu özellik alanın dize değerini sunucu ve uygulama arasında iletir. Ayrıca, **Gerçek** tür alanları için para birimi olarak biçimlendirilen alanlar için de kullanılır. Bu alanlar için, özellik para birimi kodunu uygulamaya geçirmek amacıyla kullanılır.

### <a name="datevalue-date"></a>dateValue (tarih)

**Tarih** türü alanlar için bu özellik alanın tarih değerini sunucu ve uygulama arasında iletir.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Zaman çizelgesi girişi bölümünde özel alanı gösterir ve kaydeder

Aşağıda, zaman çizelgesi girdi oluşturmayla ilgili mobil uygulamadan alınan bir ekran görüntüsü vardır. Kullanıma hazır alanları ve "test dizesi" adı verilen "Ikinci seçenek" bölümünde zaten ayarlanmış olan bir özel alanı "İkinci seçenek" olarak gösterir.

![Uygulamadaki sınama dizesi özel alanı](media/timesheet-entry.jpg)



"Test dizesi" özel alanı için kullanılabilen enum seçeneklerinden birini seçerek, kullanıcının mobil uygulamasına ait bir ekran görüntüsü aşağıdadır.  Bu iki seçenek, radyo düğmeleri olarak gösterilen "İlk seçenek" ve "İkinci seçenek"dir. İkinci seçenek şu anda seçilidir.

![Test dizesi özel alanı için seçenek düğmeleri (radyo düğmeleri)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>TSTimesheetLine tablosunu, özel bir alana sahip olacağı şekilde genişletin

Tipik senaryolarda, zaman çizelgesi girişi bölümündeki özel bir alan için veriler TSTimesheetLine tablosuna kaydedilmesinden kaynaklanıyor olabilir. Ancak, veriler sağlanan TSTimesheetTrans kaydına dayalı olarak alınacaksa veya belirli bir kayıt bağlamına sahip değilse (örneğin, alan proje parametrelerinde salt okunur olarak ayarlandıysa), diğer tablolar kullanılabilir.

Özel alanların yedekleme veritabanı kayıtları içermemesi gerekmez. Bunlar, X++ mantığına dayalı olarak dinamik olarak oluşturulabilir. Bu yaklaşım, salt okunur senaryolarda yararlı olabilir (dinamik olarak oluşturulmuş özel alan değerleri örneği için, TSTimesheetDetails sınıfındaki komut zinciri, buildCustomFieldListForHeader yöntemi).

Aşağıda Visual Studio'da yer alan Uygulama Nesne Ağacı bir ekran görüntüsü bulunmaktadır. TSTimesheetLine tablosunun bir uzantısını, TestLineString alanı özel alanı olarak eklenmiştir.

![Satır dizesi](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Zaman çizelgesi girişi bölümünde bir alan göstermek için TSTimesheetSettings sınıfının buildCustomFieldList yönteminde komut zinciri kullanın

Bu kod, uygulamadaki alanla ilgili görüntü ayarlarını denetler. Örneğin, alan türünü, etiketini, alanın zorunlu olup olmayacağını ve alanın hangi bölümünde göründüğünü kontrol eder.

Aşağıdaki örnek zaman girişlerinde bir dize alanını gösterir. Bu alan, seçenek düğmeleri (radyo düğmeleri) ile **İlk seçenek** ve **İkinci seçenek** olan iki seçenek bulunur. Uygulamadaki alan, TSTimesheetLine tablosuna eklenen **TestLineString** alanıyla ilişkilendirilir.

**TSTimesheetCustomField::newFromMetatdata()** yönteminin özel alana başlatılmasını basitleştirilmiş: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ve **numberOfDecimals**. Bu parametreleri, dilerseniz el ile de ayarlayabilirsiniz.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>TSTimesheetEntry sınıfının buildCustomFieldListForEntry yönteminde bir komut zinciri kullanarak bir zaman çizelgesi girişine değerleri girin.

**buildCustomFieldListForEntry** yöntemi, mobil uygulamadaki kaydedilmiş zaman çizelgesi satırlarına değer girmek için kullanılır. Bir TSTimesheetTrans kaydını parametre olarak alır. Bu kayıttaki alanlar uygulamadaki özel alan değerini doldurmak için kullanılabilir.

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Bir zaman çizelgesi girdisini veritabanından veritabanına geri kaydetmek için TSTimesheetEntryService sınıfında zincir komutunu kullanın

Bir özel alanı normal kullanım sırasında veritabanına geri kaydetmek için, birden çok yöntemi genişletmeniz gerekir:

- **timesheetLineNeedsUpdating** yöntemi, satır kaydının uygulamadaki Kullanıcı tarafından değiştirilip değiştirilmediğini ve veritabanına kaydedilmesi gerekip alınmayacağını belirlemek için kullanılır. Performans sorun değilse, bu yöntem her zaman **doğru** dönen şekilde basitleştirilebilir.
- **populateTimesheetLineFromEntryDuringCreate** ve **populateTimesheetLineFromEntryDuringUpdate** yöntemleri uzatılabilecek ve TSTimesheetLine'deki TSTimesheetEntry veritabanı kaydına değer girmeleri için genişletilebilir sağlanan veri sözleşme kaydı. Aşağıdaki örnekte, veritabanı alanı ile giriş alanı arasındaki eşlemenin X++ kodu aracılığıyla el ile nasıl yapıldığı konusunda dikkat edin.
- **populateTimesheetWeekFromEntry** yöntemi, **TSTimesheetEntry** nesnesiyle eşlenen özel alan TSTimesheetLineweek veritabanı tablosuna geri yazması gerekiyorsa da genişletilebilir.

> [!NOTE]
> Aşağıdaki örnek kullanıcının veritabanına seçtiğini **firstOption** veya **secondOption** değerini bir ham dize değeri olarak kaydeder. Veritabanı alanı **Enum** türünde bir alan ise, bu değerler el ile bir Enum değeriyle eşleştirilebilir ve veritabanı tablosundaki bir Enum alanına kaydedilebilir.

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Zaman çizelgesi başlık bölümünde bir özel alan göster

Aşağıda, kullanıcı bir zaman çizelgesi görüntüleme ilgili mobil uygulamadan alınan bir ekran görüntüsü vardır. Sağ üst köşedeki "Daha fazla bilgi" düğmesi, "Daha fazla ayrıntı görüntüle" seçeneği gösterilsin şekilde seçildi.  

![Diğer ayrıntıları görüntüle komutu](media/show-more.png)



Aşağıda, bir zaman çizelgesinin "Daha fazla" bölümünü gösterir ilgili mobil uygulamadan alınan bir ekran görüntüsü vardır. Zaman çizelgesi başlığı bölümüne, "Bu zaman çizelgesinin kullanım oranı (hesaplanan özel alan)" adında bir özel alan eklenmiştir. Özel alanda "0,667" salt okunur değeri ayarlandı.

![Daha fazla bölümü](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>TSTimesheetTable tablosunu, özel bir alana sahip olacağı şekilde genişletin

Tipik senaryolarda, başlık bölümündeki özel bir alan için veriler TSTimesheetHeader tablosuna çekilmesinden kaynaklanıyor olabilir. Ancak, veriler sağlanan TSTimesheetTable kaydına dayalı olarak alınacaksa veya belirli bir kayıt bağlamına sahip değilse (örneğin, alan proje parametrelerinde salt okunur olarak ayarlandıysa), diğer tablolar kullanılabilir.

Özel alanların yedekleme veritabanı kayıtları içermemesi gerekmez. Bunlar, X++ mantığına dayalı olarak dinamik olarak oluşturulabilir. Aşağıdaki örnek bu yaklaşımı gösterir.

Üst bilgi bölümündeki alanlar uygulamada her zaman salt okunurdur.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Başlık bölümünde bir alan göstermek için TSTimesheetSettings sınıfının buildCustomFieldList yönteminde komut zinciri kullanın

Bu kod, uygulamadaki alanla ilgili görüntü ayarlarını denetler. Örneğin, alan türünü, etiketini, alanın zorunlu olup olmayacağını ve alanın hangi bölümünde göründüğünü kontrol eder.

Aşağıdaki örnek, uygulamadaki başlık bölümünde hesaplanan bir değeri gösterir.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>TSTimesheetDetails sınıfının buildCustomFieldListForHeader yönteminde bir komut zinciri kullanarak bir zaman çizelgesi ayrıntıları değerleri girin.

**buildCustomFieldListForHeader** yöntemi, mobil uygulamadaki zaman çizelgesi başlık ayrıntılarını doldurmak için kullanılır. Bir TSTimesheetTable kaydını parametre olarak alır. Bu kayıttaki alanlar uygulamadaki özel alan değerini doldurmak için kullanılabilir. Aşağıdaki örnek, veritabanından herhangi bir değeri okumaz. Bunun yerine, uygulama içinde gösterilen bir hesaplanmış değer oluşturmak için X++ mantığını kullanır.


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Diğer yapılandırılabilirlik/genişletilebilirlik fırsatları

### <a name="adding-additional-validation-for-the-app"></a>Uygulama için ek doğrulama ekleniyor

Veritabanı düzeyindeki zaman çizelgesi işlevselliği için varolan mantık yine de beklendiği gibi çalışır. Kaydetme veya gönderme işlemlerinin tamamlanmasını durdurmak ve belirli bir hata iletisini göstermek için, komut uzantısı zinciri yoluyla koda **hata ver ("kullanıcıya ileti")** ekleyebilirsiniz. İşte yararlı genişletilebilir yöntemlerine üç örnek:

- **validateWrite**, TSTimesheetLine tablosunda kaydetme işlemi sırasında bir zaman çizelgesi satırı için **yanlış** dönerse, bir hata mesajı mobil uygulamada görüntülenir.
- **validateSubmit**, TSTimesheetTable tablosunda bir zaman çizelgesi için uygulamaya gönderme sırasında **yanlış** dönerse, bir hata mesajı kullanıcıya görüntülenir.
- TSTimesheetLine tablosundaki **insert** yöntemi sırasında alanları dolduran (örneğin, **satır özelliği**) mantık çalışmaya devam eder.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Kullanıma alan alanları konfigürasyon aracılığıyla salt okunur gizleme ve işaretleme

Proje parametrelerinden, kullanıma hazır alanları mobil uygulamada salt okunur veya gizli yapabilirsiniz. **Proje yönetimi ve hesap oluşturma parametreleri** sayfasının **zaman çizelgesi** sekmesindeki **mobil zaman çizelgeleri** bölümünde bulunan seçenekleri ayarlayın.

![Proje parametreleri](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Uzantılar aracılığıyla seçim için kullanılabilen etkinlikleri değiştirme

**getActivitiesForProject()** ve **getActivityQuery()** yöntemleri ile **TsTimesheetProjectService** sınıfında doldurulan bir proje için seçimde kullanılabilen etkinlikler. Belirli bir proje için kullanılabilir olan etkinlikler için bu davranışı iş senaryonuz ile eşleştirmek üzere değiştirmek için komut zinciri kullanabilirsiniz.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Zaman çizelgesi girişlerine varsayılan proje kategorisi girme

Zaman çizelgesi girişlerinde varsayılan proje kategorisi girişi üç düzeyde gerçekleşir. İstenen davranışı elde etmek için bu düzeylerin herhangi birinin veya tümünün davranışını uzatmak amacıyla komut zinciri kullanabilirsiniz. Aşağıdaki hiyerarşisi kullanılır:

1. Uygulama, proje kaynağındaki varsayılan kategoriyi yerleştirmeye çalışır. Bu varsayılan kategori **getCurrentUserResource** ve **getDelegatedResourcesForCurrentUser** yöntemleri, **TSTimesheetSettingsService** sınıfında ayarlanmıştır.
2. Proje kaynak düzeyinde varsayılan kategori sağlanmamışsa, uygulama bunu proje etkinliğinden almaya çalışır. Bu varsayılan kategori, **TSTimesheetProjectService** sınıfının **getActivitiesForProject** yönteminde ayarlanmıştır.
3. Proje etkinlik düzeyinde varsayılan kategori sağlanmamışsa, varsayılan kategori proje parametrelerinden alınır. Bu varsayılan kategori, **TSTimesheetProjectService** sınıfının **getProjectDetailsbyRule** yönteminde ayarlanmıştır.
