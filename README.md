# Custom Code Standart Rules For [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)

[![Latest Version on Packagist][badge-packagist-version]][link-packagist]
[![PHP Version][badge-php-version]](link-github)
[![Total Downloads][badge-total-downloads]][link-packagist]
[![Software License][badge-license]](LICENSE)

<!--

Some rules used in this pattern can be found in the following repositories:

* [Slevomat Coding Standard](https://github.com/slevomat/coding-standard/)
* [Object Calisthenics](https://github.com/object-calisthenics/phpcs-calisthenics-rules/)

-->

## Install

> **Requires [PHP 7.2+](https://php.net/releases/)**

To get started with `php-coding-standard`, use Composer to add the package to your project's dependencies:

```bash
composer require allysonsilva/php-coding-standard --dev
```

## Sniffs

> Use the command to check the amount of sniffs in Coding Standard applied:

```bash
./vendor/bin/phpcs --standard=PSR12 -e
// or
./vendor/bin/phpcs --standard=Generic -e
```

> Use the command to view documentation for any specific sniffs:

```bash
./vendor/bin/phpcs --standard=PSR12 --sniffs=PSR12.Namespaces.CompoundNamespaceDepth --generator=text
// or
./vendor/bin/phpcs --standard=Squiz --sniffs=Squiz.Classes.SelfMemberReference --generator=text
```

**The `AppStandard` standard contains 168 sniffs:**

```
Generic (39 sniffs)
-------------------
  Generic.Arrays.ArrayIndent
  Generic.Arrays.DisallowLongArraySyntax
  Generic.Classes.DuplicateClassName
  Generic.CodeAnalysis.EmptyPHPStatement
  Generic.CodeAnalysis.EmptyStatement
  Generic.CodeAnalysis.UnconditionalIfStatement
  Generic.CodeAnalysis.UnnecessaryFinalModifier
  Generic.CodeAnalysis.UnusedFunctionParameter
  Generic.CodeAnalysis.UselessOverridingMethod
  Generic.ControlStructures.InlineControlStructure
  Generic.Files.ByteOrderMark
  Generic.Files.InlineHTML
  Generic.Files.LineEndings
  Generic.Files.LineLength
  Generic.Files.OneClassPerFile
  Generic.Files.OneInterfacePerFile
  Generic.Files.OneObjectStructurePerFile
  Generic.Files.OneTraitPerFile
  Generic.Formatting.DisallowMultipleStatements
  Generic.Formatting.SpaceAfterCast
  Generic.Formatting.SpaceAfterNot
  Generic.Functions.CallTimePassByReference
  Generic.Functions.FunctionCallArgumentSpacing
  Generic.NamingConventions.UpperCaseConstantName
  Generic.PHP.CharacterBeforePHPOpeningTag
  Generic.PHP.DeprecatedFunctions
  Generic.PHP.DisallowAlternativePHPTags
  Generic.PHP.DisallowShortOpenTag
  Generic.PHP.ForbiddenFunctions
  Generic.PHP.LowerCaseConstant
  Generic.PHP.LowerCaseKeyword
  Generic.PHP.LowerCaseType
  Generic.Strings.UnnecessaryStringConcat
  Generic.WhiteSpace.ArbitraryParenthesesSpacing
  Generic.WhiteSpace.DisallowTabIndent
  Generic.WhiteSpace.IncrementDecrementSpacing
  Generic.WhiteSpace.LanguageConstructSpacing
  Generic.WhiteSpace.ScopeIndent
  Generic.WhiteSpace.SpreadOperatorSpacingAfter

ObjectCalisthenics (9 sniffs)
-----------------------------
  ObjectCalisthenics.Classes.ForbiddenPublicProperty
  ObjectCalisthenics.CodeAnalysis.OneObjectOperatorPerLine
  ObjectCalisthenics.Files.ClassTraitAndInterfaceLength
  ObjectCalisthenics.Files.FunctionLength
  ObjectCalisthenics.Metrics.MaxNestingLevel
  ObjectCalisthenics.Metrics.MethodPerClassLimit
  ObjectCalisthenics.Metrics.PropertyPerClassLimit
  ObjectCalisthenics.NamingConventions.ElementNameMinimalLength
  ObjectCalisthenics.NamingConventions.NoSetter

PEAR (4 sniffs)
---------------
  PEAR.Commenting.InlineComment
  PEAR.Functions.ValidDefaultValue
  PEAR.WhiteSpace.ObjectOperatorIndent
  PEAR.WhiteSpace.ScopeClosingBrace

PSR1 (3 sniffs)
---------------
  PSR1.Classes.ClassDeclaration
  PSR1.Files.SideEffects
  PSR1.Methods.CamelCapsMethodName

PSR12 (16 sniffs)
-----------------
  PSR12.Classes.AnonClassDeclaration
  PSR12.Classes.ClassInstantiation
  PSR12.Classes.ClosingBrace
  PSR12.ControlStructures.BooleanOperatorPlacement
  PSR12.ControlStructures.ControlStructureSpacing
  PSR12.Files.DeclareStatement
  PSR12.Files.FileHeader
  PSR12.Files.ImportStatement
  PSR12.Files.OpenTag
  PSR12.Functions.NullableTypeDeclaration
  PSR12.Functions.ReturnTypeDeclaration
  PSR12.Keywords.ShortFormTypeKeywords
  PSR12.Namespaces.CompoundNamespaceDepth
  PSR12.Operators.OperatorSpacing
  PSR12.Properties.ConstantVisibility
  PSR12.Traits.UseDeclaration

PSR2 (9 sniffs)
---------------
  PSR2.Classes.ClassDeclaration
  PSR2.Classes.PropertyDeclaration
  PSR2.ControlStructures.ElseIfDeclaration
  PSR2.ControlStructures.SwitchDeclaration
  PSR2.Files.ClosingTag
  PSR2.Files.EndFileNewline
  PSR2.Methods.FunctionCallSignature
  PSR2.Methods.FunctionClosingBrace
  PSR2.Methods.MethodDeclaration

SlevomatCodingStandard (48 sniffs)
----------------------------------
  SlevomatCodingStandard.Arrays.TrailingArrayComma
  SlevomatCodingStandard.Classes.ClassConstantVisibility
  SlevomatCodingStandard.Classes.DisallowLateStaticBindingForConstants
  SlevomatCodingStandard.Classes.EmptyLinesAroundClassBraces
  SlevomatCodingStandard.Classes.ModernClassNameReference
  SlevomatCodingStandard.Classes.TraitUseSpacing
  SlevomatCodingStandard.Classes.UnusedPrivateElements
  SlevomatCodingStandard.Classes.UselessLateStaticBinding
  SlevomatCodingStandard.Commenting.DocCommentSpacing
  SlevomatCodingStandard.Commenting.ForbiddenAnnotations
  SlevomatCodingStandard.Commenting.ForbiddenComments
  SlevomatCodingStandard.Commenting.InlineDocCommentDeclaration
  SlevomatCodingStandard.ControlStructures.ControlStructureSpacing
  SlevomatCodingStandard.ControlStructures.LanguageConstructWithParentheses
  SlevomatCodingStandard.ControlStructures.NewWithParentheses
  SlevomatCodingStandard.ControlStructures.RequireNullCoalesceOperator
  SlevomatCodingStandard.ControlStructures.RequireShortTernaryOperator
  SlevomatCodingStandard.Exceptions.DeadCatch
  SlevomatCodingStandard.Functions.UnusedInheritedVariablePassedToClosure
  SlevomatCodingStandard.Functions.UnusedParameter
  SlevomatCodingStandard.Functions.UselessParameterDefaultValue
  SlevomatCodingStandard.Namespaces.AlphabeticallySortedUses
  SlevomatCodingStandard.Namespaces.NamespaceDeclaration
  SlevomatCodingStandard.Namespaces.NamespaceSpacing
  SlevomatCodingStandard.Namespaces.ReferenceUsedNamesOnly
  SlevomatCodingStandard.Namespaces.RequireOneNamespaceInFile
  SlevomatCodingStandard.Namespaces.UnusedUses
  SlevomatCodingStandard.Namespaces.UseDoesNotStartWithBackslash
  SlevomatCodingStandard.Namespaces.UseFromSameNamespace
  SlevomatCodingStandard.Namespaces.UseSpacing
  SlevomatCodingStandard.Namespaces.UselessAlias
  SlevomatCodingStandard.Operators.RequireCombinedAssignmentOperator
  SlevomatCodingStandard.Operators.SpreadOperatorSpacing
  SlevomatCodingStandard.PHP.OptimizedFunctionsWithoutUnpacking
  SlevomatCodingStandard.PHP.ShortList
  SlevomatCodingStandard.PHP.TypeCast
  SlevomatCodingStandard.PHP.UselessSemicolon
  SlevomatCodingStandard.TypeHints.DeclareStrictTypes
  SlevomatCodingStandard.TypeHints.LongTypeHints
  SlevomatCodingStandard.TypeHints.NullTypeHintOnLastPosition
  SlevomatCodingStandard.TypeHints.NullableTypeForNullDefaultValue
  SlevomatCodingStandard.TypeHints.ParameterTypeHintSpacing
  SlevomatCodingStandard.TypeHints.ReturnTypeHintSpacing
  SlevomatCodingStandard.TypeHints.TypeHintDeclaration
  SlevomatCodingStandard.TypeHints.UselessConstantTypeHint
  SlevomatCodingStandard.Variables.DuplicateAssignmentToVariable
  SlevomatCodingStandard.Variables.UnusedVariable
  SlevomatCodingStandard.Variables.UselessVariable

Squiz (40 sniffs)
-----------------
  Squiz.Arrays.ArrayBracketSpacing
  Squiz.Arrays.ArrayDeclaration
  Squiz.Classes.ClassFileName
  Squiz.Classes.LowercaseClassKeywords
  Squiz.Classes.SelfMemberReference
  Squiz.Classes.ValidClassName
  Squiz.Commenting.DocCommentAlignment
  Squiz.Commenting.FunctionComment
  Squiz.Commenting.FunctionCommentThrowTag
  Squiz.ControlStructures.ControlSignature
  Squiz.ControlStructures.ForEachLoopDeclaration
  Squiz.ControlStructures.ForLoopDeclaration
  Squiz.ControlStructures.LowercaseDeclaration
  Squiz.Functions.FunctionDeclaration
  Squiz.Functions.FunctionDeclarationArgumentSpacing
  Squiz.Functions.GlobalFunction
  Squiz.Functions.LowercaseFunctionKeywords
  Squiz.Functions.MultiLineFunctionDeclaration
  Squiz.NamingConventions.ValidVariableName
  Squiz.Operators.ValidLogicalOperators
  Squiz.PHP.GlobalKeyword
  Squiz.PHP.InnerFunctions
  Squiz.PHP.LowercasePHPFunctions
  Squiz.PHP.NonExecutableCode
  Squiz.Scope.MethodScope
  Squiz.Scope.StaticThisUsage
  Squiz.Strings.ConcatenationSpacing
  Squiz.Strings.DoubleQuoteUsage
  Squiz.Strings.EchoedStrings
  Squiz.WhiteSpace.CastSpacing
  Squiz.WhiteSpace.ControlStructureSpacing
  Squiz.WhiteSpace.FunctionOpeningBraceSpace
  Squiz.WhiteSpace.FunctionSpacing
  Squiz.WhiteSpace.LanguageConstructSpacing
  Squiz.WhiteSpace.LogicalOperatorSpacing
  Squiz.WhiteSpace.ObjectOperatorSpacing
  Squiz.WhiteSpace.ScopeClosingBrace
  Squiz.WhiteSpace.ScopeKeywordSpacing
  Squiz.WhiteSpace.SemicolonSpacing
  Squiz.WhiteSpace.SuperfluousWhitespace
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## License

The MIT License (MIT). Please see [License File](LICENSE) for more information.

### Happy coding!

[badge-total-downloads]: https://img.shields.io/packagist/dt/allysonsilva/php-coding-standard.svg?style=for-the-badge&label=Total+downloads
[badge-packagist-version]: https://img.shields.io/packagist/v/allysonsilva/php-coding-standard.svg?style=for-the-badge&label=Latest
[badge-php-version]: https://img.shields.io/packagist/php-v/allysonsilva/php-coding-standard.svg?style=for-the-badge&logo=php&label=PHP&color=474A8A&labelColor=787CB5&logoColor=white
[badge-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=for-the-badge

[link-packagist]: https://packagist.org/packages/allysonsilva/php-coding-standard
[link-github]: https://github.com/allysonsilva/php-coding-standard
