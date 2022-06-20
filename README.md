# FCC_REACT


Items.defaultProps = { quantity: 0};          // set default props

Items.propTypes ={ quantity: PropTypes.number.isRequired }            //Define the Props as a number (need to import PropTypes from 'prop-types')


class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      visibility: false
    };
this.toggleVisibility = this.toggleVisibility.bind(this)              //менять стейт по нажатию кнопки
  }
toggleVisibility(){
  this.setState(state => ({
visibility: !state.visibility
  })) 
}
  render() {
    if (this.state.visibility) {
      return (
        <div>
          <button onClick={this.toggleVisibility}>Click Me</button>
          <h1>Now you see me!</h1>
        </div>
      );
    } else {
      return (
        <div>
          <button onClick={this.toggleVisibility}>Click Me</button>
        </div>
      );
    }
  }
}

///////////////////////////////////////////////////////////////////////
class ControlledInput extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: ''
    };
this.handleChange=this.handleChange.bind(this)              //input
  }
handleChange(event){
  this.setState({
    input: event.target.value
  })
}
  render() {
    return (
      <div>
<input value ={this.state.input} onChange = {this.handleChange} />
        <h4>Controlled Input:</h4>
        <p>{this.state.input}</p>
      </div>
    );
  }
};

///////////////////////////////////////////////////
                              componentWillMount()                    method is called before the render()
                              
                              componentDidMount().                  This method is called after a component is mounted to the DOM
                              
                              
                              
