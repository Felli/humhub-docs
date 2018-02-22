Snippets
=================

Snippets are self contained panels which can be added to the sidebar of for example the space or dashboard layout.

### Dashboard Layout
Adding the following in your module's `config.php` file will enable the view of your snippet on your dashboard.

```php
namespace humhub\modules\yourmodule;

use humhub\widgets\BaseMenu;

return [
    'id' => 'yourmodule',
    'class' => 'humhub\modules\yourmodule\Module',
    'namespace' => 'humhub\modules\yourmodule',
    'events' => [
        ['class' => humhub\modules\space\widgets\Sidebar::className(), 'event' => BaseMenu::EVENT_INIT, 'callback' => ['humhub\modules\yourmodule\Module', 'onDashboardSidebarInit']],
  ],
];
```

### Space Layout
Adding the following in your module's `config.php` file will enable the view of your snippet in your Spaces.

```php
namespace humhub\modules\yourmodule;

use humhub\widgets\BaseMenu;

return [
    'id' => 'yourmodule',
    'class' => 'humhub\modules\yourmodule\Module',
    'namespace' => 'humhub\modules\yourmodule',
    'events' => [
        ['class' => humhub\modules\space\widgets\Sidebar::className(), 'event' => BaseMenu::EVENT_INIT, 'callback' => ['humhub\modules\yourmodule\Events', 'onSpaceSidebarInit']],
  ],
];
```
