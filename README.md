# HJ 代码片段

## 基础代码

### `im`

```typescript
import xxx;
```

### `imp`

```typescript
import xx from xxx
```

### `imd`

```typescript
import { xx } from xxx
```

### `ime`

```typescript
import * as xx from xxx
```

### `ima`

```typescript
import { xx as xxx } from xxxx
```

### `exp`

```typescript
export default xxx;
```

### `exd`

```typescript
export { xx } from xxx
```

### `exa`

```typescript
export { xx as xxx } from xxxx
```

### `dob`

```typescript
const { xx } = xxx;
```

### `dar`

```typescript
const [xx] = xxx;
```

### `cfun`

```typescript
const xx = (xxx) => {};
```

### `clg`

```typescript
console.log("xx: ", xx);
```

### `cer`

```typescript
console.error("xx: ", xx);
```

### `useeffect`

```typescript
useEffect(() => {}, []);
```

### `usestate`

```typescript
const [xx, setXx] = useState(xxx);
```

### `useref`

```typescript
const xx = useRef();
```

### `usecallback`

```typescript
const xx = useCallback(() => {}, []);
```

### `usememo`

```typescript
const xx = useMemo(() => {}, []);
```

### `usenav`

```ts
const navigation = useNavigation();
```

### `useroute`

```ts
const { params } = useRoute();
```

### `rf`

```ts
import React from 'react'

const Example = props => {
  return <div>hello world<div>
}

export default Example
```

### `rfi`

```ts
import React, { FC } from 'react'

interface IProps {}

const Example: FC<IProps> = props => {
  return <div>hello world<div>
}

export default Example

```

### `rff`

```ts
import React, { forwardRef, useImperativeHandle } from 'react'

export interface IExampleRef {}

interface IProps {}

const Example: React.ForwardRefRenderFunction<IExampleRef, IProps> = (
  props,
  ref,
) => {
  useImperativeHandle(ref, () => ({})

  return <div>hello world</div>
}

export default forwardRef(Example)

```

## 业务代码

### `columns`

```ts
const columns: ColumnsType<any> = [
  { title: "title", dataIndex: "name" },
  {
    title: "操作",
    dataIndex: "action",
    render: (_, row) => {
      return (
        <ActionText.Group>
          <ActionText status="primary" text="编辑" to="/components" />
        </ActionText.Group>
      );
    },
  },
];
```

### `usetable`

```ts
const { tableProps, form, submit, reset, refresh } = useTablePagingGQL({
  formatParams: (values) => {
    const { page, ...val } = values;
    return {
      input: {
        ...val,
        ...page,
      },
    };
  },
  gql: ExampleDocument,
  gqlKey: "example",
});
```

### `formsearch`

```ts
<Form form={form}>
  <SearchFormLayout.Row>
    <SearchFormLayout.Col>
      <Form.Item label="label" name="label">
        <Input />
      </Form.Item>
    </SearchFormLayout.Col>
    <SearchFormLayout.Col>
      <Form.Item>
        <SearchFormLayout.Space>
          <Button type="primary">搜索</Button>
          <Button type="default">重置</Button>
        </SearchFormLayout.Space>
      </Form.Item>
    </SearchFormLayout.Col>
  </SearchFormLayout.Row>
</Form>
```

### `forminput`

```ts
<Form.Item label="label" name="name">
  <Input />
</Form.Item>
```

### `formtext`

```ts
<Form.Item label="label" name="name">
  <Input.TextArea />
</Form.Item>
```

### `formselect`

```ts
<Form.Item label="label" name="name">
  <Select options={[]} />
</Form.Item>
```

### `formasync`

```ts
<Form.Item label="label" name="label">
  <AsyncSelect
    remote={{
      gqlKey: "example",
      gql: ExampleDocument,
    }}
  />
</Form.Item>
```

### `fromcheck`

```ts
<Form.Item label="label" name="name" valuePropName="checked">
  <Checkbox>content</Checkbox>
</Form.Item>
```

### `fromnumber`

```ts
<Form.Item label="label" name="name">
  <InputNumber />
</Form.Item>
```

### `formswitch`

```ts
<Form.Item label="label" name="name" valuePropName="checked">
  <Switch />
</Form.Item>
```

### `fromradio`

```ts
<Form.Item label="label" name="name">
  <Radio.Group>
    <Radio value="a">item 1</Radio>
    <Radio value="b">item 2</Radio>
  </Radio.Group>
</Form.Item>
```

### `formdate`

```ts
<Form.Item label="label" name="name">
  <DatePicker />
</Form.Item>
```

### `fromrange`

```ts
<Form.Item label="label" name="name">
  <DatePicker.RangePicker />
</Form.Item>
```

### `formbutton`

```ts
<Form.Item>
  <Button type="primary" htmlType="submit" onClick={() => ({})}>
    submit
  </Button>
  <Button htmlType="button" onClick={() => ({})}>
    reset
  </Button>
</Form.Item>
```
