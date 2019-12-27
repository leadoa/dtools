# dtools
邓辉用的工具
Tree工具：将表格列表数组转成树状结构

安装： composer require leadoa/dtools

need your config/app.php add Prettus\Repository\Providers\RepositoryServiceProvider::class to the end of the providers array:

'providers' => [
    ...
    Leadoa\Dtools\DtoolsProvider::class,
],

	'Dtree' => Leadoa\Dtools\Facades\Dtree::class,

使用：
use Leadoa\Dtools\Facades\Dtree;

$as = $menus->toArray();
$rs = Dtree::makeTree($as);
dd($rs);

