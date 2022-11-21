+ p + ps

+ pageNum ( currentPage ) + pageSize (numPerPage)



```
public class BaseConditionVO {
    // 页面显示条目数，默认10
    public final static int PAGE_SHOW_COUNT = 20;
    // 页码，默认第一页
    public int pageNum = 1;
    // 页面个数 默认20
    public int pageSize = 0;
    // 总条目
    public int totalCount = 0;
    // 排序字段
    public String orderField;
    // 排序顺序
    public String orderDirection;
    // 关键字
    public String keywords;
    // 查询状态
    public String status;
    // 查询类型
    public String type;
    // 查询开始时间
    public Date startDate;
    // 查询结束时间
    public Date endDate;
    //省略其他的get，set方法

    //注意
    public int getStartIndex() {
        int pageNum = this.getPageNum() > 0 ? this.getPageNum() - 1 : 0;
        return pageNum * this.getPageSize();
    }

}
```



```
<div class="pagination" targetType="navTab" totalCount="200" numPerPage="20" pageNumShown="10" currentPage="2"></div>

```



