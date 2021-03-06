.. index::
   single: Forms; Fields; country

Type de champ Country
=====================

Le type ``country`` est un sous-ensemble de ``ChoiceType`` qui affiche la liste
des pays du monde. Et en bonus, les noms des pays sont affichés dans la langue de
l'utilisateur.

La « valeur » de chaque pays est son code en 2 lettres.

.. note::

   La locale de l'utilisateur est retournée par la méthode :phpmethod:`Locale::getDefault()`

Contrairement au type ``choice``, vous n'avez pas besoin de spécifier les options
``choices`` ou ``choice_list`` puisque le type retourne automatiquement la liste
de tous les pays du monde. Vous *pouvez* spécifier ces options manuellement, mais alors
vous devriez plutôt utiliser directement le type ``choice``.

+-------------+------------------------------------------------------------------------+
| Rendu comme | peut être différentes balises (voir :ref:`forms-reference-choice-tags`)|
+-------------+------------------------------------------------------------------------+
| Options     | - `choices`_                                                           |
| surchargées |                                                                        |
+-------------+------------------------------------------------------------------------+
| Options     | - `multiple`_                                                          |
| héritées    | - `expanded`_                                                          |
|             | - `preferred_choices`_                                                 |
|             | - `empty_value`_                                                       |
|             | - `error_bubbling`_                                                    |
|             | - `error_mapping`_                                                     |
|             | - `empty_data`_                                                        |
|             | - `required`_                                                          |
|             | - `label`_                                                             |
|             | - `label_attr`_                                                        |
|             | - `data`_                                                              |
|             | - `read_only`_                                                         |
|             | - `disabled`_                                                          |
|             | - `mapped`_                                                            |
+-------------+------------------------------------------------------------------------+
| Type parent | :doc:`choice</reference/forms/types/choice>`                           |
+-------------+------------------------------------------------------------------------+
| Classe      | :class:`Symfony\\Component\\Form\\Extension\\Core\\Type\\CountryType`  |
+-------------+------------------------------------------------------------------------+

Options surchargées
-------------------

choices
~~~~~~~

**default**: ``Symfony\Component\Intl\Intl::getRegionBundle()->getCountryNames()``

La valeur par défaut de l'option ``choices`` est la liste des pays.
Il utilise la langue par défaut pour déterminer quelle langue utiliser.

Options héritées
----------------

Ces options héritent du type :doc:`choice</reference/forms/types/choice>` :

.. include:: /reference/forms/types/options/multiple.rst.inc

.. include:: /reference/forms/types/options/expanded.rst.inc

.. include:: /reference/forms/types/options/preferred_choices.rst.inc

.. include:: /reference/forms/types/options/empty_value.rst.inc

.. include:: /reference/forms/types/options/error_bubbling.rst.inc

.. include:: /reference/forms/types/options/error_mapping.rst.inc

Ces options héritent du type :doc:`field</reference/forms/types/form>` :

.. include:: /reference/forms/types/options/empty_data.rst.inc

.. include:: /reference/forms/types/options/required.rst.inc

.. include:: /reference/forms/types/options/label.rst.inc

.. include:: /reference/forms/types/options/label_attr.rst.inc

.. include:: /reference/forms/types/options/data.rst.inc

.. include:: /reference/forms/types/options/read_only.rst.inc

.. include:: /reference/forms/types/options/disabled.rst.inc

.. include:: /reference/forms/types/options/mapped.rst.inc