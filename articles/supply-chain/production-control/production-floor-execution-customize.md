---
title: Üretim katı yürütme arabirimini özelleştirme
description: Bu konu, geçerli formların nasıl genişletileceğini veya üretim katı yürütme arabirimi için yeni form ve düğmelerin nasıl oluşturulacağını açıklamaktadır.
author: johanhoffmann
ms.date: 05/04/2022
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ad5037442f27a5068b38613655591f1298808eac
ms.sourcegitcommit: 28537b32dbcdefb1359a90adc6781b73a2fd195e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712957"
---
# <a name="customize-the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimini özelleştirme

[!include [banner](../includes/banner.md)]

Geliştiriciler, geçerli formları genişletebilir veya üretim katı yürütme arabirimi için yeni form ve düğmeleri oluşturabilir. Bu yeni öğelere ait kodu ekledikten sonra, yöneticiler veya atölye yöneticileri bunları arabirime standart konfigürasyon denetimlerini kullanarak kolayca ekleyebilirler.

Örneğin, ana formda yeni sütunlar gerekiyorsa, olası çözümlerden bazıları şunlardır:

- `JmgProductionFloorExecutionMainGrid` formunu genişletin ve istenen alanları ekleyin.
- Yeni bir form oluşturun ve bunu yeni bir ana görünüm olarak ekleyin (sekme).

## <a name="add-a-new-button-action"></a>Yeni düğme ekleyin (eylem)

Yeni bir düğme (eylem) eklemek için, aşağıdaki adımları izleyerek özel eyleminizi uygulayan sınıfı oluşturun.

1. `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action` adlı yeni bir sınıf oluşturun;

    - `<ExtensionPrefix>` genellikle şirket adınızı kullanarak çözümünüzü benzersiz olarak tanımlar.
    - `<ActionName>` sınıf için benzersiz bir addır. Genellikle eylemin türünü tanımlar.

1. Yeni sınıf, `JmgProductionFloorExecutionAction` sınıfını genişletmelidir.
1. Gerekli tüm yöntemleri geçersiz kılın.

Örnekler için aşağıdaki sınıfların koduna bakın:

- `JmgProductionFloorExecutionBreakAction`- Herhangi bir kayıt gerektirmeyen basit eylem sınıfı.
- `JmgProductionFloorExecutionReportFeedbackAction` - Daha karmaşık işlevler sağlayan bir sınıf.

Bitirdiğinizde, yeni düğme (eylem) otomatik olarak Microsoft Dynamics 365 Supply Chain Management içindeki **Tasarım sekmeleri** sayfasında listelenecektir. Burada, siz (veya bir yönetici veya kat yöneticisi), standart düğmeleri ekleyebilir, tıpkı kolayca birincil veya ikincil araç çubuğuna eklendiği gibi. Talimatlar için bkz. [Üretim katı yürütme arabirimini tasarlama](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Yeni ana görünüm ekleme

1. İstenen öğelere ve işlevlere sahip yeni bir form oluşturun. Bu formun bir uzantı değil yeni bir biçim olduğunu unutmayın. Formu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>` olarak adlandırın;

    - `<ExtensionPrefix>` genellikle şirket adınızı kullanarak çözümünüzü benzersiz olarak tanımlar.
    - `<FormName>` form için benzersiz bir addır.

1. `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>` adlı bir menü öğesi oluşturun.
1. Listeye yeni menü öğesi ekleyerek `getMainMenuItemsList` yönteminin genişletilmiş olduğu, `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` adlı bir uzantı oluşturun. Aşağıdaki kodda bir örneği gösterilmiştir.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionMenuItemProvider))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Bitirdiğinizde, yeni ana görünüm Supply Chain Management'ndeki **Tasarım sekmeleri** sayfasındaki **Ana görünüm** kombo kutusunda otomatik olarak listelenecektir. Burada, siz (veya bir yönetici veya kat yöneticisi), bunu yeni veya mevcut sekmelere ekleyebilir, tıpkı standart ana görünümlere eklendiği gibi. Talimatlar için bkz. [Üretim katı yürütme arabirimini tasarlama](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Ayrıntılar görünümü ekleme

1. İstenen öğelere ve işlevlere sahip yeni bir form oluşturun. Bu formun bir uzantı değil yeni olduğunu unutmayın. Formu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail` olarak adlandırın; 

    - `<ExtensionPrefix>` genellikle şirket adınızı kullanarak çözümünüzü benzersiz olarak tanımlar.
    - `<FormName>` form için benzersiz bir addır.

1. `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail` adlı bir menü öğesi oluşturun.
1. Listeye yeni menü öğesi ekleyerek `getDetailsMenuItemList` yönteminin genişletilmiş olduğu, `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` adlı bir uzantı oluşturun.

Bitirdiğinizde, yeni ayrıntılar görünüm Supply Chain Management'ndeki **Tasarım sekmeleri** sayfasındaki **Ayrıntılar görünümü** kombo kutusunda otomatik olarak listelenecektir. Burada, siz (veya bir yönetici veya kat yöneticisi), bunu yeni veya mevcut sekmelere ekleyebilir, tıpkı standart ayrıntılar görünümlerine eklendiği gibi. Talimatlar için bkz. [Üretim katı yürütme arabirimini tasarlama](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Forma veya diyaloğa sayısal tuş takımı ekleme

Aşağıdaki örnekte, sayısal anahtar tuşlarının bir forma nasıl ekleneceği gösterilmiştir.

1. Her bir formun içerdiği sayısal tuş takımı denetleyicilerinin sayısı, o formdaki sayısal tuşların sayısına eşit olmalıdır.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Her bir sayısal tuş takımı denetleyicisinin davranışını ayarlayın ve her sayısal tuş takımı denetleyicisini sayısal tuş takımı formunun bir bölümüne bağlayın.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Açılan diyalog olarak sayısal tuş takımı kullan

Aşağıdaki örnekte, bir açılan diyalog için sayısal tuş takımı denetleyicisi ayarlamak için bir yol gösterilir.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Aşağıdaki örnekte, bir açılan sayısal tuş takımı iletişim kutusunu çağırmak için bir yol gösterilir.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="add-a-date-and-time-controls-to-a-form-or-dialog"></a>Forma veya iletişim kutusuna tarih ve saat denetimleri ekleme

Bu bölüm, bir forma veya iletişim kutusuna tarih ve saat denetimlerinin nasıl ekleneceğini gösterir. Dokunmatik kullanımı kolay tarih ve saat denetimleri çalışanların tarih ve saat belirtmelerine olanak tanır. Aşağıdaki ekran görüntüleri, denetimlerin sayfada normal olarak nasıl göründüğünü gösterir. Saat denetimi hem 12 saatlik hem de 24 saatlik sürümleri sağlar; gösterilen sürüm, arabirimin altında çalıştığı kullanıcı hesabı için belirlenen tercihi izler.

![Tarih denetimi örneği.](media/pfe-customize-date-control.png "Tarih denetimi örneği")

![12 saatlik sürümü gösteren zaman denetimi örneği.](media/pfe-customize-time-control-12h.png "12 saatlik sürümü gösteren zaman denetimi örneği")

![24 saatlik sürümü gösteren zaman denetimi örneği.](media/pfe-customize-time-control-24h.png "24 saatlik sürümü gösteren zaman denetimi örneği")

Aşağıdaki prosedür, bir forma tarih ve saat denetimlerinin nasıl ekleneceği hakkında bir örnek gösterir.

1. Formun içereceği her bir tarih ve saat denetimi için forma bir denetleyici ekleyin. (Denetleyici sayısı formdaki tarih ve saat denetimleri sayısına eşit olmalıdır.)

    ```xpp
    private JmgProductionFloorExecutionDateTimeController  dateFromController; 
    private JmgProductionFloorExecutionDateTimeController  dateToController; 
    private JmgProductionFloorExecutionDateTimeController  timeFromController; 
    private JmgProductionFloorExecutionDateTimeController  timeToController;
    ```

1. Gerekli değişkenleri (`utcdatetime` türünde) bildirin.

    ```xpp
    private utcdatetime fromDateTime;
    private utcdatetime toDateTime;
    ```

1. Tarih saatin tarih saat denetleyicileri tarafından güncelleştirileceği yöntemler oluşturun. Aşağıdaki örnekte bu tür bir yöntem gösterilmiştir.

    ```xpp
    private void setFromDateTime(utcdatetime _value)
        {
            fromDateTime = _value;
        }
    ```

1. Her bir tarih saat denetleyicisinin davranışını ayarlayın ve her denetleyiciyi formun bir bölümüne bağlayın. Aşağıdaki örnek, başlangıç tarihi ve başlangıç zamanı denetimleri için verilerin nasıl ayarlanacağını gösterir. Bitiş tarihi ve bitiş zamanı denetimleri için (gösterilmez) benzer bir kod ekleyebilirsiniz.

    ```xpp
    /// <summary>
    /// Initializes all date and time controllers, defines their behavior, and connects them with the form parts.
    /// </summary>
    private void initializeDateControlControllers()
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        timeFromController = new JmgProductionFloorExecutionDateTimeController();
        timeFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        timeFromController.parmDateTimeValue(fromDateTime);
        
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, timeFromController);
        TimeFromFormPart.getPartFormRun().setTimeControlController(timeFromController, dateFromController);
        
        ...

    }
    ```

    Tek ihtiyacınız olan bir tarih denetimi ise, zaman denetimi kurulumunu atlayabilir ve bunun yerine aşağıdaki örnekte gösterildiği şekilde sadece tarih denetimini ayarlayabilirsiniz:

    ```xpp
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, null);
    }
    ```

## <a name="additional-resources"></a>Ek kaynaklar

- [Üretim katı yürütme arabirimini düzenleme](production-floor-execution-styles.md)
- [Üretim katı yürütme arabirimini tasarlama](production-floor-execution-tabs.md)
