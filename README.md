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
