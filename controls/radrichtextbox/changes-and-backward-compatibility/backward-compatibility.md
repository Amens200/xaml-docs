---
title: Backward Compatibility
page_title: Backward Compatibility
description: Backward Compatibility
slug: radrichtextbox-backward-compatibility
tags: backward,compatibility
published: True
position: 1
---

# Backward Compatibility



This article will list the breaking changes and how they can be fixed when upgrading to a specific version of the controls to the next one.

## What's Different in 2014 Q1 - 2014.1.0226

There are no breaking changes in this version of the control.

## What's Different in 2013 Q3 - 2013.3.1016

### Changed

As of Q3 2013 the assembly references required for RadRichTextBox to work have changed. Two additional assemblies are now needed -
              __Telerik.Windows.Documents.Flow.dll__ and __Telerik.Windows.Documents.Core.dll__.
            

More about all required assembly references you can find [here]({%slug radrichtextbox-frequently-asked-questions%}).
            

### What to do now

Add references to __Telerik.Windows.Documents.Flow.dll__ and __Telerik.Windows.Documents.Core.dll__.
            

### Changed

Some of RadDocument's public methods were obsoleted and they will be removed in one of the future releases. Among those are the
              __Insert~()__ and __Delete~()__ methods and all other methods that intervene with the document directly.
            

### What to do now

Manipulating the document directly causes different issues, including clearing of the History stack. Instead of using the obsoleted methods the
              recommended way to edit a document is through RadRichTextBox. In scenarios when you do not want to show a RadRichTextBox and want to manipulate the
              document from code you can use [RadDocumentEditor]({%slug radrichtextbox-features-raddocumenteditor%}).
            

### Changed

Change in the IFontPropertiesDialog interface so that the dialog could be populated with the values of the CurrentSpanStyle. Custom implementations of
              the dialog will not work.
            

### What to do now

Use the properties of FontPropertiesDialogContext:
            

-ApplyStyle as the callback.
            

-CurrentEditingStyle as the style to populate the dialog on showing it.
            

### Changed

* Telerik.Windows.Documents.Layout.SubStringPosition class has been removed.

* Telerik.Windows.Documents.Model.AnchorStyles class has been removed.

* Telerik.Windows.Documents.Layout.RadTextMeasurerSL has been removed.

### What to do now

The above are no longer needed and you should not use them.

### Changed

The float Telerik.Windows.Documents.Layout.RadTextMeasurer.GetBaseLineOffset(string fontFamlily) method has been removed.

### What to do now

The method is for internal use only.

## What's Different in 2013 Q2 - 2013.2.611

There are no breaking changes in this version of the control.

## What's Different in 2013 Q1 - 2013.2.0220

There are breaking changes related to the discontinued support of the RadRibbonBar control. The predefined UI of RadRichTextBox can now only be based on RadRibbonView.

## What's Different in 2012 Q3 - 2012.3.1017

There are no breaking changes in this version of the control.

## What's Different in 2012 Q2 - 2012.2.0607

* When creating a __Table__ programatically it no longer has a predefined set of borders.
            The default style of a __Table__ is __TableNormal__. It does not inherit other styles, does not contain predefined borders and is the one applied when creating a table programmatically.
            When creating a table from the UI, the __TableGrid__ style is applied. It has a predefined set of borders and can be applied programmatically as follows:
            

#### __C#__

{{region radrichtextbox-radrichtextbox-backward-compatibility_0}}
	        table.StyleName = RadDocumentDefaultStyles.DefaultTableGridStyleName;
	{{endregion}}

More about __Styles__ can be found in [this topic]({%slug radrichtextbox-features-styles%}).
            

## What's Different in 2012 Q1 - 2012.1.0215

There are no breaking changes in this version of the control.

# See Also