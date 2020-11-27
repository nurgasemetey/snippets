###  react router location does not exist on type


[Property 'from' does not exist on type '{}' · Issue #41674 · DefinitelyTyped/DefinitelyTyped](https://github.com/DefinitelyTyped/DefinitelyTyped/issues/41674 "Property 'from' does not exist on type '{}' · Issue #41674 · DefinitelyTyped/DefinitelyTyped")



[Reach Router and TypeScript: Property 'path' does not exist on type 'IntrinsicAttributes &amp; IntrinsicClassAttributes&lt;SignupPage&gt; &amp; Readonly&lt;{ children?: ReactNode; }&gt; ... · Issue #141 · reach/router](https://github.com/reach/router/issues/141 "Reach Router and TypeScript: Property 'path' does not exist on type 'IntrinsicAttributes &amp; IntrinsicClassAttributes&lt;SignupPage&gt; &amp; Readonly&lt;{ children?: ReactNode; }&gt; ... · Issue #141 · reach/router")


 

```
import { RouteComponentProps } from 'react-router-dom';


interface IProps extends RouteComponentProps {
}

interface IState {
    days: any[],
    input: string,
    exists: boolean
}

const dateFormat = "YYYY-MM-DD";
const email = "test@gmail.com"

export class MainDecisionContainer extends React.Component<IProps, IState> {


<Menu style={{ float: 'right' }} theme="dark" mode="horizontal" defaultSelectedKeys={[this.props.location.pathname]}>
                            <Menu.Item key="/">This Week</Menu.Item>
                            <Menu.Item key="2">Previous decisions</Menu.Item>
                            <SubMenu key="SubMenu" icon={<SettingOutlined />} title="Settings">
                                <Menu.Item key="setting:1">Logout</Menu.Item>
                            </SubMenu>
                        </Menu>



```
