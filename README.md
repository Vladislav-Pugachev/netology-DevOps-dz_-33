# 1.
> 1
> >resource и data_source перечислены в terraform-provider-aws/internal/provider/provider.go
-  resource c 868 ао 1987
-  data_source с 412 по 866 

> 2
> > Конфликт с name_prefix
```
		"name": {
			Type:          schema.TypeString,
			Optional:      true,
			Computed:      true,
			ForceNew:      true,
			ConflictsWith: []string{"name_prefix"},
```

>> name описано в выражении и должно быть не более 80 знаков
```
re = regexp.MustCompile(`^[a-zA-Z0-9_-]{1,80}$`)
```
