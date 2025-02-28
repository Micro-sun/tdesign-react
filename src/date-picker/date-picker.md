:: BASE_DOC ::

## API
### DatePicker Props

名称 | 类型 | 默认值 | 说明 | 必传
-- | -- | -- | -- | --
className | String | - | 类名 | N
style | Object | - | 样式，TS 类型：`React.CSSProperties` | N
allowInput | Boolean | false | 是否允许输入日期 | N
clearable | Boolean | false | 是否显示清除按钮 | N
disableDate | Object / Array / Function | - | 禁用日期，示例：['A', 'B'] 表示日期 A 和日期 B 会被禁用。`{ from: 'A', to: 'B' }` 表示在 A 到 B 之间的日期会被禁用。`{ before: 'A', after: 'B' }` 表示在 A 之前和在 B 之后的日期都会被禁用。其中 A = '2021-01-01'，B = '2021-02-01'。值类型为 Function 则表示返回值为 true 的日期会被禁用。TS 类型：`DisableDate` `type DisableDate = Array<DateValue> | DisableDateObj | ((date: DateValue) => boolean)` `interface DisableDateObj { from?: string; to?: string; before?: string; after?: string }`。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
disabled | Boolean | - | 是否禁用组件 | N
enableTimePicker | Boolean | false | 是否显示时间选择 | N
firstDayOfWeek | Number | - | 第一天从星期几开始。可选项：1/2/3/4/5/6/7 | N
format | String | undefined | 用于格式化日期，全局配置默认为：'YYYY-MM-DD'，[详细文档](https://day.js.org/docs/en/display/format) | N
inputProps | Object | - | 透传给输入框（Input）组件的参数。TS 类型：`InputProps`，[Input API Documents](./input?tab=api)。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
mode | String | date | 选择器模式。可选项：year/quarter/month/week/date | N
placeholder | String / Array | undefined | 占位符。TS 类型：`string` | N
popupProps | Object | - | 透传给 popup 组件的参数。TS 类型：`PopupProps`，[Popup API Documents](./popup?tab=api)。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
prefixIcon | TElement | - | 用于自定义组件前置图标。TS 类型：`TNode`。[通用类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/common.ts) | N
presets | Object | - | 预设快捷日期选择，示例：`{ '元旦': '2021-01-01', '昨天':  dayjs().subtract(1, 'day').format('YYYY-MM-DD'), '特定日期': () => ['2021-02-01'] }`。TS 类型：`PresetDate` `interface PresetDate { [name: string]: DateValue | (() => DateValue) }`。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
presetsPlacement | String | bottom | 预设面板展示区域（包含确定按钮）。可选项：left/top/right/bottom | N
status | String | - | 输入框状态。可选项：default/success/warning/error | N
suffixIcon | TElement | - | 用于自定义组件后置图标。TS 类型：`TNode`。[通用类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/common.ts) | N
timePickerProps | Object | - | 透传 TimePicker 组件属性。TS 类型：`TimePickerProps`，[TimePicker API Documents](./time-picker?tab=api)。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
tips | TNode | - | 输入框下方提示文本，会根据不同的 `status` 呈现不同的样式。TS 类型：`string | TNode`。[通用类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/common.ts) | N
value | String / Number / Array / Date | '' | 选中值。TS 类型：`DateValue` `type DateValue = string | number | Date`。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
defaultValue | String / Number / Array / Date | '' | 选中值。非受控属性。TS 类型：`DateValue` `type DateValue = string | number | Date`。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
onBlur | Function |  | TS 类型：`(context: { value: DateValue; e: FocusEvent }) => void`<br/>当输入框失去焦点时触发 | N
onChange | Function |  | TS 类型：`(value: DateValue, context: { dayjsValue?: Dayjs, trigger?: DatePickerTriggerSource }) => void`<br/>选中值发生变化时触发。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts)。<br/>`import { Dayjs } from 'dayjs'`<br/><br/>`type DatePickerTriggerSource = 'confirm' | 'pick' | 'enter' | 'preset' | 'clear'`<br/> | N
onFocus | Function |  | TS 类型：`(context: { value: DateValue; e: FocusEvent }) => void`<br/>输入框获得焦点时触发 | N
onPick | Function |  | TS 类型：`(value: DateValue) => void`<br/>面板选中值后触发 | N

### DateRangePicker Props

名称 | 类型 | 默认值 | 说明 | 必传
-- | -- | -- | -- | --
className | String | - | 类名 | N
style | Object | - | 样式，TS 类型：`React.CSSProperties` | N
allowInput | Boolean | false | 是否允许输入日期 | N
clearable | Boolean | false | 是否显示清楚按钮 | N
disableDate | Object / Array / Function | - | 禁用日期，示例：['A', 'B'] 表示日期 A 和日期 B 会被禁用。{ from: 'A', to: 'B' } 表示在 A 到 B 之间的日期会被禁用。{ before: 'A', after: 'B' } 表示在 A 之前和在 B 之后的日期都会被禁用。其中 A = '2021-01-01'，B = '2021-02-01'。值类型为 Function 则表示返回值为 true 的日期会被禁用。TS 类型：`DisableRangeDate` `type DisableRangeDate = Array<DateValue> | DisableDateObj | ((context: { date: DateRangeValue; partial: DateRangePickerPartial }) => boolean)` `interface DisableDateObj { from?: string; to?: string; before?: string; after?: string }` `type DateRangePickerPartial = 'start' | 'end'`。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
disabled | Boolean | - | 是否禁用组件，值为数组表示可分别控制开始日期和结束日期是否禁用 | N
enableTimePicker | Boolean | false | 是否显示时间选择 | N
firstDayOfWeek | Number | - | 第一天从星期几开始。可选项：1/2/3/4/5/6/7 | N
format | String | - | 用于格式化日期，[详细文档](https://day.js.org/docs/en/display/format) | N
mode | String | date | 选择器模式。可选项：year/quarter/month/week/date | N
panelPreselection | Boolean | true | 在开始日期选中之前，面板是否显示预选状态，即是否高亮预选日期 | N
placeholder | String / Array | - | 占位符，值为数组表示可分别为开始日期和结束日期设置占位符。TS 类型：`string | Array<string>` | N
popupProps | Object | - | 透传给 popup 组件的参数。TS 类型：`PopupProps`，[Popup API Documents](./popup?tab=api)。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
prefixIcon | TElement | - | 组件前置图标。TS 类型：`TNode`。[通用类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/common.ts) | N
presets | Object | - | 预设快捷日期选择，示例：{ '特定日期范围': ['2021-01-01', '2022-01-01'], '本月': [dayjs().startOf('month'), dayjs().endOf('month')] }。TS 类型：`PresetRange` `interface PresetRange { [range: string]: DateRange | (() => DateRange)}` `type DateRange = [DateValue, DateValue]`。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
presetsPlacement | String | bottom | 预设面板展示区域（包含确定按钮）。可选项：left/top/right/bottom | N
rangeInputProps | Object | - | 透传给范围输入框 RangeInput 组件的参数。TS 类型：`RangeInputProps`，[RangeInput API Documents](./range-input?tab=api)。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
separator | String | - | 日期分隔符，支持全局配置，默认为 '-' | N
status | String | - | 输入框状态。可选项：default/success/warning/error | N
suffixIcon | TElement | - | 组件后置图标。TS 类型：`TNode`。[通用类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/common.ts) | N
timePickerProps | Object | - | 透传 TimePicker 组件属性。TS 类型：`TimePickerProps`，[TimePicker API Documents](./time-picker?tab=api)。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
tips | TNode | - | 输入框下方提示文本，会根据不同的 `status` 呈现不同的样式。TS 类型：`string | TNode`。[通用类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/common.ts) | N
value | Array | [] | 选中值。TS 类型：`DateRangeValue` `type DateRangeValue = Array<DateValue>`。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
defaultValue | Array | [] | 选中值。非受控属性。TS 类型：`DateRangeValue` `type DateRangeValue = Array<DateValue>`。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts) | N
onBlur | Function |  | TS 类型：`(context: { value: DateRangeValue; partial: DateRangePickerPartial; e: FocusEvent }) => void`<br/>当输入框失去焦点时触发 | N
onChange | Function |  | TS 类型：`(value: DateRangeValue, context: { dayjsValue?: Dayjs[], trigger?: DatePickerTriggerSource }) => void`<br/>选中值发生变化时触发。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts)。<br/>`import { Dayjs } from 'dayjs'`<br/> | N
onFocus | Function |  | TS 类型：`(context: { value: DateRangeValue; partial: DateRangePickerPartial; e: FocusEvent }) => void`<br/>输入框获得焦点时触发 | N
onInput | Function |  | TS 类型：`(context: { input: string; value: DateRangeValue; partial: DateRangePickerPartial; e: InputEvent }) => void`<br/>输入框数据发生变化时触发，参数 input 表示输入内容，value 表示组件当前有效值 | N
onPick | Function |  | TS 类型：`(value: DateValue, context: PickContext) => void`<br/>选中日期时触发，可能是开始日期，也可能是结束日期，第二个参数可以区分是开始日期或是结束日期。[详细类型定义](https://github.com/Tencent/tdesign-react/blob/develop/src/date-picker/type.ts)。<br/>`interface PickContext { e: MouseEvent; partial: DateRangePickerPartial }`<br/> | N

### DatePickerPanel Props

名称 | 类型 | 默认值 | 说明 | 必传
-- | -- | -- | -- | --
className | String | - | 类名 | N
style | Object | - | 样式，TS 类型：`React.CSSProperties` | N
`Pick<DatePickerProps, 'value' | 'defaultValue' | 'disabled' | 'disableDate' | 'enableTimePicker' | 'firstDayOfWeek' | 'format' | 'mode' | 'presets' | 'presetsPlacement' | 'timePickerProps'>` | \- | - | 继承 `Pick<DatePickerProps, 'value' | 'defaultValue' | 'disabled' | 'disableDate' | 'enableTimePicker' | 'firstDayOfWeek' | 'format' | 'mode' | 'presets' | 'presetsPlacement' | 'timePickerProps'>` 中的全部 API | N

### DateRangePickerPanel Props

名称 | 类型 | 默认值 | 说明 | 必传
-- | -- | -- | -- | --
className | String | - | 类名 | N
style | Object | - | 样式，TS 类型：`React.CSSProperties` | N
`Pick<DateRangePickerProps, 'value'| 'defaultValue' | 'disabled' | 'disableDate' | 'enableTimePicker' | 'firstDayOfWeek' | 'format' | 'mode' | 'presets' | 'presetsPlacement' | 'panelPreselection' | 'timePickerProps'>` | \- | - | 继承 `Pick<DateRangePickerProps, 'value'| 'defaultValue' | 'disabled' | 'disableDate' | 'enableTimePicker' | 'firstDayOfWeek' | 'format' | 'mode' | 'presets' | 'presetsPlacement' | 'panelPreselection' | 'timePickerProps'>` 中的全部 API | N
