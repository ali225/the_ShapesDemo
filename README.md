using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ShapesDemo.Models
{
    abstract class GeometricFigure
    {
        protected double _width;
        protected double _height;

        public virtual double Height
        {
            get { return this._height; }
            set { this._height = value; }
        }

        public virtual double Width
        {
            get { return this._width; }
            set { this._width = value; }
        }

        public double Area
        {
            get
            {
                return this.ComputeArea();
            }
        }

        public GeometricFigure(double height, double width)
        {
            this._height = height;
            this._width = width;
        }

        public abstract double ComputeArea();
    }
}
